---
title: WSL 中的 GPU 加速 - 常見問題集
description: Windows 子系統 Linux 版中的 GPU 加速常見問題
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "106965679"
---
# <a name="faq"></a><span data-ttu-id="856c5-103">常見問題集</span><span class="sxs-lookup"><span data-stu-id="856c5-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="856c5-104">如何? 啟用 DirectML 加速？</span><span class="sxs-lookup"><span data-stu-id="856c5-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="856c5-105">預設會啟用 DirectML 裝置，假設您有適當的 DirectX 12 GPU 可用。</span><span class="sxs-lookup"><span data-stu-id="856c5-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="856c5-106">如果可能的話，TensorFlow 作業會自動指派給 DirectML 裝置。</span><span class="sxs-lookup"><span data-stu-id="856c5-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="856c5-107">如果您在使用 DirectML 加速判斷模型是否正在執行時遇到問題，您可以將它放入 `tf.debugging.set_log_device_placement(True)` 程式的第一個語句，TensorFlow 就會將裝置放置資訊列印到主控台。</span><span class="sxs-lookup"><span data-stu-id="856c5-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="856c5-108">如何? 控制特定作業的裝置放置？</span><span class="sxs-lookup"><span data-stu-id="856c5-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="856c5-109">如同任何其他裝置 (請參閱 [TensorFlow 指南：使用 GPU](https://www.tensorflow.org/guide/gpu)) ，您可以使用 `tf.device()` 來控制要執行的裝置。</span><span class="sxs-lookup"><span data-stu-id="856c5-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="856c5-110">DirectML 裝置字串為 `'DML'` 。</span><span class="sxs-lookup"><span data-stu-id="856c5-110">The DirectML device string is `'DML'`.</span></span> 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="856c5-111">我有多個 Gpu。</span><span class="sxs-lookup"><span data-stu-id="856c5-111">I have multiple GPUs.</span></span> <span data-ttu-id="856c5-112">如何? 選取 DirectML 使用哪一個？</span><span class="sxs-lookup"><span data-stu-id="856c5-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="856c5-113">有幾種不同的方式可以完成這項作業，視您是否要控制整個進程或每個會話的 (或兩個) 而定。</span><span class="sxs-lookup"><span data-stu-id="856c5-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="856c5-114">如果您想要控制 TensorFlow 整個進程可以看見哪些裝置，請使用 `DML_VISIBLE_DEVICES` 環境變數。</span><span class="sxs-lookup"><span data-stu-id="856c5-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="856c5-115">如果您想要以每個會話為基礎來控制，請使用 `tf.GPUOptions.visible_device_list` 。</span><span class="sxs-lookup"><span data-stu-id="856c5-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="856c5-116">如何? 使用 `DML_VISIBLE_DEVICES` 環境變數來控制哪些 GPU () 可供 DirectML 使用？</span><span class="sxs-lookup"><span data-stu-id="856c5-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="856c5-117">TensorFlow with DirectML 支援 `DML_VISIBLE_DEVICES` 環境變數，其採用以逗號分隔的裝置識別碼清單， (也稱為「介面卡索引」 ) 。設定時，只有在 TensorFlow 整個進程的情況下，才會顯示該清單中的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="856c5-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="856c5-118">使用排除 `DML_VISIBLE_DEVICES` 的裝置不會出現在可供 TensorFlow 的實體裝置清單中。</span><span class="sxs-lookup"><span data-stu-id="856c5-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="856c5-119">以下是 **未** 設定的範例輸出 `DML_VISIBLE_DEVICES` ：</span><span class="sxs-lookup"><span data-stu-id="856c5-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="856c5-120">使用 `DML_VISIBLE_DEVICES="1"` ：</span><span class="sxs-lookup"><span data-stu-id="856c5-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="856c5-121">請注意，藉由將可見的裝置限制為只有索引 1 (AMD Radeon RX 5700 XT) ，TensorFlow 現在會將識別碼0指派給此裝置，並使其成為預設值。</span><span class="sxs-lookup"><span data-stu-id="856c5-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="856c5-122">您也可以使用此環境變數重新訂購裝置。</span><span class="sxs-lookup"><span data-stu-id="856c5-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="856c5-123">例如，設定 `DML_VISIBLE_DEVICES="1,0"` ：</span><span class="sxs-lookup"><span data-stu-id="856c5-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="856c5-124">請注意， (NVIDIA TITAN V 和 AMD Radeon RX 5700 XT) 的兩個 Gpu 現在已切換位置。</span><span class="sxs-lookup"><span data-stu-id="856c5-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="856c5-125">若要防止顯示特定的裝置，您可以 `-1` 在逗號分隔清單中提供不正確識別碼 (例如) 。</span><span class="sxs-lookup"><span data-stu-id="856c5-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="856c5-126">無效專案之後的所有裝置識別碼都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="856c5-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="856c5-127">您也可以使用此功能來完全停用 DirectML 加速。</span><span class="sxs-lookup"><span data-stu-id="856c5-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="856c5-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="856c5-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="856c5-129">如何? 使用 `visible_device_list` session 選項來控制) DirectML 用來執行會話的 GPU (？</span><span class="sxs-lookup"><span data-stu-id="856c5-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="856c5-130">類似于 `DML_VISIBLE_DEVICES` ，您也可以在工作階段層級設定類似的字串來控制可見的裝置。</span><span class="sxs-lookup"><span data-stu-id="856c5-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="856c5-131">`visible_device_list`建立 TensorFlow 會話時，可在類別上使用此屬性 `GPUOptions` 。</span><span class="sxs-lookup"><span data-stu-id="856c5-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

<span data-ttu-id="856c5-132">如需詳細資訊，您可以閱讀 [TensorFlow GPUOPTIONS API 參考](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) 。</span><span class="sxs-lookup"><span data-stu-id="856c5-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>