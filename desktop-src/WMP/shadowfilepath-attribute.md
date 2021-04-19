---
title: ShadowFilePath 屬性
description: ShadowFilePath 屬性是陰影檔案的完整路徑。
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- ShadowFilePath 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987091"
---
# <a name="shadowfilepath-attribute"></a>ShadowFilePath 屬性

**ShadowFilePath** 屬性是陰影檔案的完整路徑。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)

## <a name="remarks"></a>備註

在檔案格式轉換過程中，會建立一個 *陰影* 檔。 這是播放程式在使用者將內容從電腦同步處理到需要內容為原始檔案格式的裝置時，所使用的檔案複本。 已轉換的檔案會設定這個屬性，以指向陰影檔案的位置。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**關於轉換流程**](about-the-conversion-process.md)
</dt> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





