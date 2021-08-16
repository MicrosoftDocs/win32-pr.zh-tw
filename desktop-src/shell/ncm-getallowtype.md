---
description: 抓取指定的網路位址控制項接受的網路位址類型。
title: 'NCM_GETALLOWTYPE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858807"
---
# <a name="ncm_getallowtype-message"></a>NCM \_ GETALLOWTYPE 訊息

抓取指定的網路位址控制項接受的網路位址類型。


```C++
NCM_GETALLOWTYPE

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

傳回允許的網路位址類型作為一或多個 [**NET \_ 字串**](net-string.md) 常數。

## <a name="remarks"></a>備註

傳回的遮罩是在 [**NCM \_ GETADDRESS**](ncm-getaddress.md) 訊息中用來驗證網路位址的準則。

此訊息僅供網路位址控制使用。 若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。 請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。 這會初始化包含網路位址控制項的通用控制項程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




