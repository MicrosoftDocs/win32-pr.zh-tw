---
description: Merge 物件的 ExtractCAB 方法會從模組中解壓縮內嵌的 .cab 檔案，並將它儲存為指定的檔案。 如果此檔案不存在，安裝程式會建立此檔案，如果存在，則會覆寫該檔案。
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: 'ExtractCAB 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997631"
---
# <a name="mergeextractcab-method"></a>Merge. ExtractCAB 方法

[**Merge**](merge-object.md)物件的 **ExtractCAB** 方法會從模組中解壓縮內嵌的 .cab 檔案，並將它儲存為指定的檔案。 如果此檔案不存在，安裝程式會建立此檔案，如果存在，則會覆寫該檔案。

## <a name="syntax"></a>語法


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileName* 
</dt> <dd>

完整的目的地檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="c"></a>C++

請參閱 [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
