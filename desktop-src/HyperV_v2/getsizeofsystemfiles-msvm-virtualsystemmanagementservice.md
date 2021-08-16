---
description: 抓取虛擬機器的系統檔案大小總計。
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Msvm_VirtualSystemManagementService 類別的 GetSizeOfSystemFiles 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 385235e407cac2dd67f3dade99e4d1c834d082dfe59b541020a4548e8eea383c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392901"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 GetSizeOfSystemFiles 方法 \_

抓取虛擬機器的系統檔案大小總計。 這些包括設定和儲存的狀態檔案。

## <a name="syntax"></a>語法


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Vssd* \[在\]
</dt> <dd>

要取出其系統檔案大小之 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例的參考。 此實例可能代表虛擬機器的目前具現化，或虛擬機器快照集的實例。

</dd> <dt>

*大小* \[擴展\]
</dt> <dd>

系統檔案的總大小（以位元組為單位）。

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
</dt> </dl>

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

 

