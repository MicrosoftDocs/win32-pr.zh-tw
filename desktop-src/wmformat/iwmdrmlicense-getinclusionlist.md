---
title: 'IWMDRMLicense GetInclusionList 方法 (Wmdrmsdk .h) '
description: GetInclusionList 方法會抓取目前授權或授權鏈的整個包含清單。
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- GetInclusionList 方法 windows Media 格式
- GetInclusionList 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetInclusionList 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6389ac30d5bffeb6ad354ec6c7e83f2834921fe8fb83c1abe2bca2d0c2f43bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705238"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>IWMDRMLicense：： GetInclusionList 方法

**GetInclusionList** 方法會抓取目前授權或授權鏈的整個包含清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppGuids* \[擴展\]
</dt> <dd>

接收可識別內含技術的 Guid 陣列。

</dd> <dt>

*pcGuids* \[擴展\]
</dt> <dd>

接收 *ppGuids* 陣列中的元素數目。 陣列是使用 **CoTaskMemAlloc** 進行配置。 完成此清單之後，請呼叫 **CoTaskMemFree** 來釋放記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

授權簽發者可以指定可轉換加密內容的其他保護系統。 這個方法所抓取的 Guid 清單會識別允許的保護系統。 當您輸入 Microsoft 的授權合約以取得存根程式庫時，您將會收到目前支援的保護系統清單，以及用來識別這些系統的 Guid。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**明確授權和包含清單**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





