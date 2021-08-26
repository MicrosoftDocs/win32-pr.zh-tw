---
description: 針對此 IInkAnalysisRecognizer 可為分析結果產生的屬性，抓取 (Guid) 的全域唯一識別碼。
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer：： GetSupportedProperties 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057858"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>IInkAnalysisRecognizer：： GetSupportedProperties 方法

針對此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 可為分析結果產生的屬性，抓取 (guid) 的全域唯一識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulPropertiesCount* \[in、out\]
</dt> <dd>

*PpProperties* 中的 guid 數目。

</dd> <dt>

*ppProperties* \[擴展\]
</dt> <dd>

此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 可為分析結果產生的屬性 guid 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppProperties* 的記憶體。

 

辨識器可支援線條度量、行號、信賴等級等等。 如需辨識器可支援之屬性的完整清單，請參閱 [RecognitionProperty 常數](recognitionproperty-constants.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[RecognitionProperty 常數](recognitionproperty-constants.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

