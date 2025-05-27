原版QCustomPlot在opengl模式下，缩放会失衡

这是cpp里QCPPaintBufferGlFbo::draw里drwaImage(0,0,mGlFrameBuffer->toImage())导致的

mGlFrameBuffer是经过缩放的，一旦win下桌面缩放比例不是100%，会导致渲染尺寸不匹配

网上给出的答案都是强制修改放缩比为1，这样会导致图像模糊

我给官方发过Email，但没有回应

于是我修正了它
