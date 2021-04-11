---
description: StartService 方法會將服務放入 &\# 0034; 啟動&\# 0034; 狀態。
ms.assetid: b2b38d64-b497-46f5-8638-a9a8ce50e888
ms.tgt_platform: multiple
title: CIM_BootService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7f7f56633319f9e009f58f7c06dde7a3baee8e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936521"
---
# <a name="startservice-method-of-the-cim_bootservice-class"></a>CIM BootService 類別的 StartService 方法 \_

**StartService** 方法會將服務放在「開始」狀態。 在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。 您也可以在子類別中 **，將轉換內容轉譯** 成 **值** 陣列辨識符號的字串。 這個方法繼承自 [**CIM \_ 服務**](cim-service.md)。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
Integer StartService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。

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

[CIM \_ BootService](startservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> </dl>

 

