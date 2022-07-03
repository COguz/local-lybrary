# Yaml
Yet another Markup Language

1. [Start](#start)
1. [Comment](#comment)
1. [Dictionary](#dictionary)
1. [List](#list)
1. [Nest](#nest)

## Start

Yaml files starts with three dashes `---` 

> ```yaml
> ---
> name: My not very long yaml file
> ```

## Comment

Use hash `#` for comments

> ```yaml
> ---
> name: something
> # You can change name 
> ```

## Dictionary

Yaml dictionary contains key value pairs

> ```yaml
> ---
> name: me
> age: 12
> others: keeps going
> ```  

## List

List starts with single dash `-` or you can use python lists if you use with dictionaries

> ```yaml
> ---
> - here
> - is
> - my
> - list
> 
> mylist: ['here', 'is', 'my', 'list']
> ```

## Nest

With two spaces `  ` of indentation you can nest items

> ```yaml
> ---
> name:
>   first: me
>   second: of course me
>   third: I think that is enough name
> phone:
>   - name: phone1
>   - name: phone2
> ```
