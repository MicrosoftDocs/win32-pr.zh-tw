---
description: 調整現有虛擬硬碟的大小。
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Msvm_ImageManagementService 類別的 ResizeVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972249"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Msvm ImageManagementService 類別的 ResizeVirtualHardDisk 方法 \_

調整現有虛擬硬碟的大小。 虛擬硬碟必須離線。 請參閱此方法使用限制的備註。

## <a name="syntax"></a>語法


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

類型： **字串**

虛擬硬碟檔案的完整路徑。

</dd> <dt>

*MaxInternalSize* \[在\]
</dt> <dd>

類型： **uint64**

虛擬機器可看見的虛擬硬碟大小上限（以位元組為單位）。 *MaxInternalSize* 最小值為 *DiskSize* + 512- (*DiskSize* mod 512) 。 *DiskSize* 是虛擬硬碟檔案的大小（以位元組為單位）。 如果指定的 *MaxInternalSize* 值小於最小值，則會傳回 InvalidParameter 錯誤 (32773) 。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法可能會傳回下列其中一個值。

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

**找不到** 檔案 (32779) 
</dt> </dl>

## <a name="remarks"></a>備註

當虛擬硬碟的大小增加時，只有下列類型的虛擬硬碟可搭配此方法使用：

-   修正 VHD
-   固定 VHDX
-   動態 VHD
-   動態 VHDX
-   差異 VHDX

當虛擬硬碟的大小減少時，您只能使用下列類型的虛擬硬碟搭配此方法：

-   固定 VHDX
-   動態 VHDX
-   差異 VHDX

存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

下列 c # 範例會展開虛擬硬碟檔案。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
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

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

