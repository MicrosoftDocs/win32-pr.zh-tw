---
description: CIM CreateDirectoryAction 類別的 Invoke 方法 \_ 會採取特定的動作。 如何執行此動作的詳細資料是執行特定的。 此方法繼承自 CIM \_ 動作。
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: CIM_CreateDirectoryAction 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d2c1a79a7a662dc7c0896cec4a7c1b99248fe8538c9b7cd07203366541a6830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080002"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a>CIM CreateDirectoryAction 類別的 Invoke 方法 \_

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)類別的 **Invoke** 方法會採取特定的動作。 如何執行此動作的詳細資料是執行特定的。 此方法繼承自 [**CIM \_ 動作**](cim-action.md)。

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

在成功時傳回0的值，並傳回任何其他數位以表示錯誤。

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

[**CIM \_ CreateDirectoryAction**](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)
</dt> </dl>

 

