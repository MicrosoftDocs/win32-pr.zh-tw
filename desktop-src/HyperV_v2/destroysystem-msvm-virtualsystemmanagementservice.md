---
description: 從主機系統的管理範圍移除先前定義的虛擬機器。
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Msvm_VirtualSystemManagementService 類別的 DestroySystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850959"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 DestroySystem 方法 \_

從主機系統的管理範圍移除先前定義的虛擬機器。 也會移除任何相關聯的資源定義。 在呼叫這個方法之前，虛擬機器必須處於 [已關閉電源] 或 [已儲存] 狀態。

## <a name="syntax"></a>語法


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedSystem* \[在\]
</dt> <dd>

類型： **CIM \_** 操作一

CIM 電腦實例的參考，代表 [**要 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 終結的虛擬機器實例。

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

**不正確狀態** (5) 
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

## <a name="examples"></a>範例

下列 c # 範例會使用 **DestroySystem** 方法來移除已規劃的虛擬機器。 這段程式碼取自 [hyper-v 規劃的虛擬機器範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。

> [!IMPORTANT]
> 若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

