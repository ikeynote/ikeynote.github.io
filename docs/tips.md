### VIM
```
> :%s/<C-r><C-w>/{your_new_word}/g
> # % takes the search globally.
>
> 使用*向前搜索，使用#向后搜索光标下的单词。启动搜索后，可以使用n在相同方向上重复搜索，或使用N在相反方向上重复搜索。或者再次使用*或#来代替您所使用的单词。
>
> *和#命令基本上启动搜索，就像您使用/\<word\>或?\<word\>一样。因此，可以在/或?搜索提示符下使用向上箭头键调用这些搜索。
```

### Git
```
.. code:: python

> git add .
> git commit -m "msg"
> git push
>
> git fetch --all && git reset --hard origin/main && git pull
```

.. code:: python

    extensions = [
        ...
        'sphinx_rtd_theme',
    ]
