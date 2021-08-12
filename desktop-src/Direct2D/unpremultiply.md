---
title: Unpremultiply 效果
description: 使用此效果將影像從預乘的 Alpha 轉換成 unpremultiplied Alpha。
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- unpremultiply 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664876"
---
# <a name="unpremultiply-effect"></a>Unpremultiply 效果

使用此效果將影像從預乘的 Alpha 轉換成 unpremultiplied Alpha。 效果會將輸出中的每個輸入圖元取代 `P = {R, G, B, A}` 為 `P' = {R/A, G/A, B/A, A}` 。

此效果沒有屬性。

這項效果的 CLSID 是 CLSID \_ D2D1Unpremultiply。

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖大小與輸入點陣圖大小相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
