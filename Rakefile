# frozen_string_literal: true

namespace :new do
	desc "Membuat postingan baru"
	task :post do
	  name = ENV["TITLE"]

	  abort "rake new_page TITLE=\"whatever\"" unless name

	  slug = name.gsub(/[^\w\d]/, '-').gsub(/--/, '-')
	  now = Time.now
	  date = now.strftime("%Y-%m-%d")
	  File.open("_posts/#{date}-#{slug}.markdown", 'w') do |f|
	    f.write <<-NEWPOST
---
layout: post
title: "#{name}"
categories: 
author: Nama yang ada di weblog.rubyonrails.org jika mengambil dari sumber eksternal
translator: Nama Kamu
published: true
date: #{now.strftime("%Y-%m-%d %H:%M:%S %:z")}
---
Konten posting dalam format Markdown. Direkomendasikan menggunakan Markdown (.md, .markdown) dan hindari penulisan HTML kecuali ada sesuatu yang ingin di embed
    NEWPOST
	  end
	end
end

desc "Bantuan"
task :help do
  puts <<HELP
Semua proses ini ditangani oleh rake, berikut daftar lengkapnya:

#{%x[rake -T]}

Contoh:
  $ rake new:post TITLE="Judul Postingan"

Panduan dasar untuk jekyll:
  Untuk build sumber kode:
  $ jekyll build

  Untuk melihat hasil build:
  $ jekyll serve


Panduan lengkap untuk jekyll:

###########################################################################################
#{%x[jekyll -h]}
###########################################################################################


Referensi
- https://github.com/github/pages-gem

HELP
end

task default: "help"
