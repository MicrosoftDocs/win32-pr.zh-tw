---
description: 從增強型影片轉譯器 (EVR) 篩選要求新的輸入範例。
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: 'EC_SAMPLE_NEEDED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0058f8d0b7f8404a59f8c7e4fc5a4029c5ebaf4bc4f5c1b2678b1ed8c0f4f90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686118"
---
# <a name="ec_sample_needed"></a>\_需要 EC 範例 \_

從 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) 篩選要求新的輸入範例。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

需要新輸入之輸入資料流程的識別碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

EVR 篩選器的混音器會在需要新的輸入範例時傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> </dl>

 

 




