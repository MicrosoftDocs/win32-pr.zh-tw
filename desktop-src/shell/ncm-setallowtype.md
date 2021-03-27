---
description: 設定指定的網路位址控制項接受的網路位址類型。
title: 'NCM_SETALLOWTYPE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691204"
---
# <a name="ncm_setallowtype-message"></a>NCM \_ SETALLOWTYPE 訊息

設定指定的網路位址控制項接受的網路位址類型。


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*addrMask* \[在\]
</dt> <dd>將網路位址類型指定為一或多個 <a href="net-string.md">**NET \_ 字串**</a> 常數。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，否則傳回錯誤值。

## <a name="remarks"></a>備註

遮罩集是在 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息中用來驗證網路位址的準則。

此訊息僅供網路位址控制使用。 若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。 請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。 這會初始化包含網路位址控制項的通用控制項程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




