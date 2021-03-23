---
title: 使用 Direct3D 11、Direct3D 10 和 Direct2D
description: 本節涵蓋使用舊版 Direct3D 和 Direct2D 的 interop 技術、Direct3D 11on12 API，以及從 Direct3D 11 到 Direct3D 12 的移植指導方針。
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103612"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a>使用 Direct3D 11、Direct3D 10 和 Direct2D

本節涵蓋使用舊版 Direct3D 和 Direct2D 的 interop 技術、Direct3D 11on12 API，以及從 Direct3D 11 到 Direct3D 12 的移植指導方針。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Direct3D 12 Interop](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | D3D12 可以用來撰寫元件化應用程式。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Direct3D 11 on 12](direct3d-11-on-12.md)<br/>                                             | D3D11On12 是一種機制，開發人員可以使用 D3D11 介面和物件來驅動 D3D12 API。 D3D11on12 可讓使用 D3D11 撰寫的元件 (例如，D2D 文字和 UI) 與以 D3D12 API 為目標的元件一起運作。 D3D11on12 也可讓應用程式從 D3D11 增量移植至 D3D12，方法是讓應用程式的某些部分繼續以較簡單的目標為目標，同時讓其他人以 D3D12 為效能，同時一律具有完整且正確的呈現。 D3D11On12 可讓您更輕鬆地使用 interop 技術來共用資源，並在兩個 Api 之間同步處理工作。 <br/> |
| [從 Direct3D 11 移植到 Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md)<br/> | 本節提供從自訂 Direct3D 11 圖形引擎移植到 Direct3D 12 的一些指引。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)
</dt> </dl>

 

 





