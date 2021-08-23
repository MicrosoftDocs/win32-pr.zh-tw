---
title: MetadataPicture. mimeType
description: MimeType 屬性會捕獲中繼資料影像的標準 MIME 類型。
ms.assetid: dde541e3-ddbc-437e-a3a8-64a116e122e0
keywords:
- MetadataPicture. mimeType Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture.mimeType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9cfc6607bc121b18b7d8550576b84d251dd7f2812094a51464265e4135fa0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647698"
---
# <a name="metadatapicturemimetype"></a>MetadataPicture. mimeType

**MimeType** 屬性會捕獲中繼資料影像的標準 MIME 類型。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**getItemInfoByType** ( *name*、 *language*、 *index*) 。**mimeType**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MetadataPicture 物件**](metadatapicture-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





