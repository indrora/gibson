+++
title = '{{ replace (strings.TrimLeft "1234567890-" .File.ContentBaseName) "-" " " | title }}'
date = {{ .Date }}
draft = true
episode = {{ default 999 ( index ( findRE `\A[0-9]+` .File.ContentBaseName 1) 0 ) | int }}
tags = []
+++

