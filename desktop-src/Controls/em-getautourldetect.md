---
title: 'EM_GETAUTOURLDETECT 訊息 (Richedit .h) '
description: 指出是否已在 rich edit 控制項中開啟自動 URL 偵測。
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025181"
---
# <a name="em_getautourldetect-message"></a>EM \_ GETAUTOURLDETECT 訊息

指出是否已在 rich edit 控制項中開啟自動 URL 偵測。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果自動 URL 偵測為使用中，則傳回值為1。

如果自動 URL 偵測為非使用中，則傳回值為0。

## <a name="remarks"></a>備註

開啟自動 URL 偵測時，Microsoft Rich Edit 會持續檢查輸入的文字是否有有效的 URL。 Rich Edit 可辨識以這些首碼開頭的 Url：

-   http:
-   file：
-   mailto:
-   Ftp：
-   ip-HTTPs
-   開頭
-   nntp
-   普洛斯彼羅：
-   Telnet：
-   新聞：
-   wais
-   前景：

Rich Edit 也可辨識開頭為的標準路徑名稱 \\ \\ 。 當 Rich Edit 找出 URL 時，它會變更 URL 文字色彩、將文字加上底線，並使用 [En-us \_ 連結](en-link.md)通知用戶端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EN \_ 連結](en-link.md)
</dt> </dl>

 

 





