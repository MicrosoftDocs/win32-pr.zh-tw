---
title: ITsSbTarget TargetName 屬性
description: 指定或抓取目標的名稱。
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- TargetName 屬性遠端桌面服務
- TargetName 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，TargetName 屬性
- TargetName 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，TargetName 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971ae66d162464c49d7eb4206f1fbddf206707c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467865"
---
# <a name="itssbtargettargetname-property"></a>ITsSbTarget：： TargetName 屬性

指定或抓取目標的名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

指定目標名稱的 **BSTR** 變數。

## <a name="remarks"></a>備註

在 Windows Server 2012 之前，此屬性是唯讀的。

## <a name="requirements"></a>規格需求




| | |最低支援用戶端<br /> |無支援<br /> | |最低支援伺服器<br /> |Windows Server 2012<br /> | |IDL<br /> | <dl><dt>Sbtsv .idl</dt></dl> | |IID<br /> |IID_ITsSbTarget 定義為：<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





