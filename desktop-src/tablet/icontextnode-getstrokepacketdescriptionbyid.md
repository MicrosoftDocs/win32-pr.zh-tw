---
description: 取得陣列，其中包含指定之筆劃的封包屬性識別碼。
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'ICoNtextNode：： GetStrokePacketDescriptionById 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970623"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>ICoNtextNode：： GetStrokePacketDescriptionById 方法

取得陣列，其中包含指定之筆劃的封包屬性識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

筆劃的識別碼。

</dd> <dt>

*pulStrokePacketDescriptionCount* \[in、out\]
</dt> <dd>

每個封包中的封包屬性數目。

</dd> <dt>

*ppStrokePacketDescriptionGuids* \[擴展\]
</dt> <dd>

陣列，包含封包屬性識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppStrokePacketDescriptionGuids* 的記憶體。

 

\**ppStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述筆劃中每個點所包含的封包資料類型。 如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

