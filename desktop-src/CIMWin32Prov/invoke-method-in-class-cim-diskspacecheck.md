---
description: CIM DiskSpaceCheck 類別的 Invoke 方法會 \_ 評估特定檢查。 方法會在 CIM 內容中評估特定檢查的詳細資料，由非抽象 CIM \_ 檢查子類別描述。
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: CIM_DiskSpaceCheck 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbcef752bf412ea255891dd0f5abdf7563f0e078
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972127"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a>CIM DiskSpaceCheck 類別的 Invoke 方法 \_

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)類別的 **Invoke** 方法會評估特定檢查。 方法會在 CIM 內容中評估特定檢查的詳細資料，由非抽象 [**cim \_ 檢查**](cim-check.md) 子類別描述。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Invoke();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。

## <a name="remarks"></a>備註

這個方法目前不是由 WMI 所執行。 若要使用這個方法，您必須在自己的提供者中加以執行。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[CIM \_ DiskSpaceCheck](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> </dl>

 

