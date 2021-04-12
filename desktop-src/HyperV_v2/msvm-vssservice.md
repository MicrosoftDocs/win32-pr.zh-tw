---
description: 代表來賓 VSS 服務。 它是用來查詢來自 Hyper-v 主機的來賓叢集資訊。
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Msvm_VssService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318084"
---
# <a name="msvm_vssservice-class"></a>Msvm \_ VssService 類別

代表來賓 VSS 服務。 它是用來查詢來自 Hyper-v 主機的來賓叢集資訊。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a>成員

**Msvm \_ VssService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Msvm \_ VssService** 類別具有這些方法。



| 方法                                                                               | 描述                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) | 查詢從 Hyper-v 主機到來賓的叢集資訊。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




