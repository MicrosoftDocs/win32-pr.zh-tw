---
title: 不透明度中繼資料效果
description: 您可以使用此效果將輸入影像的區域標記為不透明，因此可能會對圖形進行內部呈現優化。
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105449"
---
# <a name="opacity-metadata-effect"></a>不透明度中繼資料效果

您可以使用此效果將輸入影像的區域標記為不透明，因此可能會對圖形進行內部呈現優化。

> [!Note]  
> 這種效果不會將影像本身修改為不透明。 它會修改與影像相關聯的資料，讓轉譯器假設指定的區域不透明。

 

這項效果的 CLSID 是 CLSID \_ D2D1OpacityMetadata。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                 | 類型和預設值                                                             | Description                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA 的 \_ 主張 \_ 輸入不透明的 \_ \_ RECT <br/> | D2D1 \_ 向量 \_ 4F<br/>  (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ MAX)  <br/> | 來源影像中不透明的部分。 預設值是整個輸入影像。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

