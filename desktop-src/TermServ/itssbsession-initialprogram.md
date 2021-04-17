---
title: ITsSbSession InitialProgram 屬性
description: 捕獲或指定此會話的初始程式。
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- InitialProgram 屬性遠端桌面服務
- InitialProgram 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，InitialProgram 屬性
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465316"
---
# <a name="itssbsessioninitialprogram-property"></a>ITsSbSession：： InitialProgram 屬性

捕獲或指定此會話的初始程式。 初始程式是在使用者會話啟動時啟動的程式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a>屬性值

包含初始程式的 **BSTR** 變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





