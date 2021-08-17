---
description: 下表描述 RecognizerCoNtext 物件事件可以引發的執行緒。EventThreadsRecognitionFires 在背景辨識執行緒上，或在呼叫 RecognizerCoNtext 物件之辨識方法的執行緒上。在背景辨識執行緒上 RecognitionWithAlternatesFires。
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: RecognizerCoNtext 物件事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091438"
---
# <a name="recognizercontext-object-events"></a>RecognizerCoNtext 物件事件

下表描述 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件事件可以引發的執行緒。



| 事件                                                                               | 執行緒                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**辨識**](inkrecognizercontext-recognition.md)                             | 在背景辨識執行緒或呼叫 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件之 [**辨識**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) 方法的執行緒上引發。<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | 在背景辨識執行緒上引發。<br/>                                                                                                                                                               |



 

 

 




