---
title: GetMuteOperation。 Completed 屬性
description: 取得或設定當 GetMuteAsync 啟動的非同步作業完成時叫用的事件處理常式。
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- 完成的屬性媒體串流 API
- 完成的屬性媒體串流 API、GetMuteOperation 介面
- GetMuteOperation 介面媒體串流 API，已完成屬性
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682177"
---
# <a name="getmuteoperationcompleted-property"></a>GetMuteOperation。 Completed 屬性

取得或設定當 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) 啟動的非同步作業完成時叫用的事件處理常式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>屬性值

事件處理常式。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

 