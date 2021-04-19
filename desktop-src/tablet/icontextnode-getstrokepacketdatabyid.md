---
description: 取得陣列，其中包含指定之筆劃的封包屬性資料。
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'ICoNtextNode：： GetStrokePacketDataById 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995821"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>ICoNtextNode：： GetStrokePacketDataById 方法

取得陣列，其中包含指定之筆劃的封包屬性資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*strokeId* \[在\]
</dt> <dd>

筆劃的識別碼。

</dd> <dt>

*pStrokePacketDataCount* \[in、out\]
</dt> <dd>

封包資料陣列的長度。

</dd> <dt>

*pplStrokePacketData* \[擴展\]
</dt> <dd>

筆劃的封包資料指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokePacketData* 的記憶體。

 

*plStrokePacketData* 包含筆劃中所有點的封包資料。 若要取得筆劃中每個點所包含的封包資料類型，請使用 [**ICoNtextNode：： GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)。

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

[**ICoNtextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

