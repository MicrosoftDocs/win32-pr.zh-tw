---
description: 在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。
title: 'NCM_DISPLAYERRORTIP 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991111"
---
# <a name="ncm_displayerrortip-message"></a>NCM \_ DISPLAYERRORTIP 訊息

在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果此訊息成功，則會 **傳回 \_ [確定]**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當輸入至控制項的位址未針對以 [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) 訊息設定的允許網路位址類型進行驗證時，請傳送此訊息以顯示錯誤訊息。 使用 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息來驗證位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




