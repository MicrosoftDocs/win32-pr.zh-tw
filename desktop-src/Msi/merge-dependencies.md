---
description: Merge 物件的 [唯讀相依性] 屬性會傳回相依性物件的集合，這些物件會列舉目前資料庫的一組未滿足的相依性。
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: 'Merge。相依性屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977702"
---
# <a name="mergedependencies-property"></a>Merge。相依性屬性

[**Merge**](merge-object.md)物件的 [唯讀相依性 **]** 屬性會傳回相依性物件 [**的集合，這些物件會**](dependency-object.md)列舉目前資料庫的一組未滿足的相依性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

不需要開啟模組就能取出相依性資訊。

### <a name="c"></a>C++

請 [**參閱 \_ 取得**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) 相依性功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
