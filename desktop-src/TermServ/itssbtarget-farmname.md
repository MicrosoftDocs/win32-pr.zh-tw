---
title: ITsSbTarget FarmName 屬性
description: 抓取或指定此目標所聯結的伺服器陣列名稱。
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- FarmName 屬性遠端桌面服務
- FarmName 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，FarmName 屬性
- FarmName 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，FarmName 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b1c36a1a44f38dac11a7e474d7fefb80a09948
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988291"
---
# <a name="itssbtargetfarmname-property"></a>ITsSbTarget：： FarmName 屬性

抓取或指定此目標所聯結的伺服器陣列名稱。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

包含伺服器陣列名稱的 **BSTR** 變數。

## <a name="requirements"></a>規格需求




| 需求 | 值 |
|--------|-------|
| 最低支援的用戶端<br /> | 都不支援<br /> | 
| 最低支援的伺服器<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv .idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget 定義為：<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





