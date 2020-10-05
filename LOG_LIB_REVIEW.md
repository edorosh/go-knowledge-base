# Log Libraries Quick Review
For one of my upcoming project I wanted to use more advanced log library instead
of the [standard](https://golang.org/pkg/log/) one. I documented my thoughts about a couple of them.

## Libraties
I reviewed the following libraries:
* [sirupsen/logrus](https://github.com/sirupsen/logrus)
* [uber-go / zap](https://github.com/uber-go/zap)
* [rs/zerolog](https://github.com/rs/zerolog)

## Comments
My result: Logrus. It’s old, not that fast but has a great community, support and is good for the beginners.

### Logrus
Old project, stable API, big community and many code examples /  integrations. It’s slow since allocates 
during logs (shouldn’t be a problem for non critical apps). Has http integration, graceful shutdown. Has no envs.

### Uber Zap
It’s fast. It supports std log interface. It defines its own API for structural logging. A poor documentation 
on integrating with http and other handlers.

### Zerolog
Takes zero allocation idea from Zap and simplifies API. Has more code examples. Has http integration and 
other handlers. Has env presets.