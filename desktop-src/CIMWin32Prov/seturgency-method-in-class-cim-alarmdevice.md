---
description: SetUrgency 方法會設定警示所需的緊急程度等級。
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: CIM_AlarmDevice 類別的 SetUrgency 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9557ad9e65b33e1ed8889ef1fd013b2d9f5426f8e819fe56608cb6846ea8669f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118172632"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>CIM AlarmDevice 類別的 SetUrgency 方法 \_

**SetUrgency** 方法會設定警示所需的緊急程度等級。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedUrgency* \[在\]
</dt> <dd>

警示閃爍、震動或發出聲音聲的相對頻率。 下列值來自 [**CIM \_ AlarmDevice**](cim-alarmdevice.md)中的 **緊迫** 屬性。

<dt>

0
</dt> <dd>

未知。

</dd> <dt>

1
</dt> <dd>

其他。

</dd> <dt>

2
</dt> <dd>

不支援。

</dd> <dt>

3
</dt> <dd>

資訊。

</dd> <dt>

4
</dt> <dd>

非關鍵性。

</dd> <dt>

5
</dt> <dd>

嚴重。

</dd> <dt>

6
</dt> <dd>

無法.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，如果不支援要求的緊急等級，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。

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

[CIM \_ AlarmDevice](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> </dl>

 

