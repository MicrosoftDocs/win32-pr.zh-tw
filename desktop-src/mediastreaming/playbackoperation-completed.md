---
title: PlaybackOperation。 Completed 屬性
description: 取得或設定當其中一個 MediaRenderer 播放方法啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、PlaybackOperation 介面
- PlaybackOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966832"
---
# <a name="playbackoperationcompleted-property"></a>PlaybackOperation。 Completed 屬性

取得或設定當其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 




