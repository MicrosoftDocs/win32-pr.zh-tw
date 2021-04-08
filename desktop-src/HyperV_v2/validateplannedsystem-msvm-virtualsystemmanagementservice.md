---
description: 驗證指定的計畫系統。
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Msvm_VirtualSystemManagementService 類別的 ValidatePlannedSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694672"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 ValidatePlannedSystem 方法 \_

驗證指定的計畫系統。 這牽涉到檢查虛擬機器設定、裝置、快照集設定、快照裝置、儲存的狀態檔案和儲存體檔案。

## <a name="syntax"></a>語法


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PlannedSystem* \[在\]
</dt> <dd>

[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)物件的參考，該物件代表要驗證的計畫系統。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> <dt>

**使用中的** 檔案 (32779) 
</dt> </dl>

## <a name="examples"></a>範例

下列 c # 範例會使用 **ValidatePlannedSystem** 方法來驗證已規劃的虛擬機器。 這段程式碼取自 [hyper-v 規劃的虛擬機器範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm)。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。

> [!IMPORTANT]
> 若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
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

 

