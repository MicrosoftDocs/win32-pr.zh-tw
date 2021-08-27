---
title: ITsSbTarget TargetLoad 屬性
description: 抓取目標的相對負載。
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- TargetLoad 屬性遠端桌面服務
- TargetLoad 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，TargetLoad 屬性
- TargetLoad 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，TargetLoad 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8224106fad6031a18bf061020a259813db639e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983921"
---
# <a name="itssbtargettargetload-property"></a>ITsSbTarget：： TargetLoad 屬性

抓取目標的相對負載。 此值是以現有和擱置中會話的數目為基礎。 根據預設，暫止的會話與現有的會話具有相同的值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>屬性值

代表目標相關負載的數位。

## <a name="remarks"></a>備註

您可以藉由設定連線代理人的 *LB \_ ConnectionEstablishmentPenalty* 參數值，來變更相對於作用中會話的暫止會話加權。 此參數位於 **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** 登錄機碼底下。 預設值為1，表示擱置會話的加權與作用中會話的加權相同。

這個屬性可在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411)的 Windows Server 2012 R2 上取得 [**ITsSbTargetEx**](itssbtargetex.md)介面。

## <a name="requirements"></a>規格需求




| 需求 | 值 |
|--------|-------|
| 最低支援的用戶端<br /> | 都不支援<br /> | 
| 最低支援的伺服器<br /> | Windows Server 2016<br /> | 
| IDL<br /> | <dl><dt>Sbtsv .idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget 定義為：<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





