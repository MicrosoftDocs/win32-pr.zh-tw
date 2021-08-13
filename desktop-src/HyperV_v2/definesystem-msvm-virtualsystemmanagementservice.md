---
description: 建立新的虛擬機器實例。
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Msvm_VirtualSystemManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47b01a2fb0935873b5a36d69376eb09bfe6d4555613c0eb8dc8907589d4f5f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645803"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 DefineSystem 方法 \_

建立新的虛擬機器實例。 未指定的屬性將會填入預設值。

## <a name="syntax"></a>語法


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SystemSettings* \[在\]
</dt> <dd>

類型： **字串**

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，可用來定義要建立之虛擬機器的屬性。 此為必要參數。

</dd> <dt>

*ResourceSettings* \[在\]
</dt> <dd>

類型：**字串 \[ \]**

許多 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例 (或) 的衍生類別。 這些實例一起說明虛擬機器的虛擬資源。 無論是否已設定此參數，都會為虛擬機器建立一組預設的裝置。 例如，系統會自動建立處理器和記憶體，並以預設值設定。

</dd> <dt>

*ReferenceConfiguration* \[在\]
</dt> <dd>

類型： **CIM \_ VirtualSystemSettingData**

參考虛擬機器設定的最上層物件之 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別實例的參考。 如果 *SystemSettings* 和 *ResourceSettings* 參數未提供個別的資訊，則會使用參考設定來補充新虛擬機器的設定。

</dd> <dt>

*ResultingSystem* \[擴展\]
</dt> <dd>

類型： **CIM \_** 操作一

[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)系統類型實例的參考，代表新建立的虛擬機器。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

類型： **CIM \_ ConcreteJob**

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

如果這個方法是以同步方式執行，它會在成功時傳回0。 如果這個方法是以非同步方式執行，它會傳回4096，而 *作業* 輸出參數可以用來追蹤非同步作業的進度。 任何其他傳回值表示錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

## <a name="remarks"></a>備註

存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

