---
title: Unpremultiply 效果
description: 使用此效果將影像從預乘的 Alpha 轉換成 unpremultiplied Alpha。
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- unpremultiply 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385061"
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
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
