---
description: 抓取 VHD 設定檔案的相關資訊。
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Msvm_ImageManagementService 類別的 GetVHDSetInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972444"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a>Msvm ImageManagementService 類別的 GetVHDSetInformation 方法 \_

抓取 VHD 設定檔案的相關資訊。

## <a name="syntax"></a>語法


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VHDSetPath* \[在\]
</dt> <dd>

指定 VHD 設定檔案位置的完整路徑。

</dd> <dt>

*AdditionalInformation* \[在\]
</dt> <dd>

陣列，指定應針對 VHD 設定檔案收集哪些額外的資訊。 陣列中的每個專案都是一種額外的資訊。 如果此參數為 Null，則不會抓取任何其他資訊。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

**路徑** (2) 


</dt> <dd></dd> </dl> </dd> <dt>

*資訊* \[擴展\]
</dt> <dd>

如果成功，此物件就會包含所要求 VHD 設定檔案的資訊。 這是 [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)的內嵌實例。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果工作已完成) ，則作業 (的參考可以是 null。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




