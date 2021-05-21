
# Docker 사용시 

## File : just-the-docs.gemspec

아래 줄에 대해 주석(#) 적용 

 - 여러 `bundler` 버전을 사용하다 보니 에러 발생한다.

```
#  spec.add_development_dependency "bundler", "~> 2.1.4"
```

## File : Gemfile

원본은 https로 되어 있으며 SSL 사용하기 복잡한 환경에서는 아래와 같이 적용한다.

```
source "http://rubygems.org"
gemspec
```


## File : nav.html

`absolute_url`을 `relative_url` 으로 변경

실제 `jekyll serve -H 0.0.0.0` 으로 실행 시 절대 경로로 `host` value를 가져오기에 Menu 포함 link 들이 모두 `http://0.0.0.0/`로 적용되기에 절대 경로를 상대경로로 변경해줄 필요가 있다.