---
description: 若要讓應用程式正常執行，主機電腦必須安裝適當的 Dll。 這些 Dll 可能是由作業系統或應用程式的可轉散發套件提供。
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: '將靜態和動態連結程式庫連結 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5c05599371521f81b488c5d3e10467a28a3c3241efd180edae15dfd40f279c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101481"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>將靜態和動態連結程式庫連結 (Direct3D 10) 

若要讓應用程式正常執行，主機電腦必須安裝適當的 Dll。 這些 Dll 可能是由作業系統或應用程式的可轉散發套件提供。

## <a name="libraries-load-appropriate-dlls"></a>程式庫載入適當的 Dll

DirectX SDK 隨附的程式庫會在執行時間自動載入適當的 Dll。 這項規則的例外狀況是 d3dx10 .lib/d3dx10d .lib，它會載入該版本 SDK 隨附的 d3dx10.dll。 例如，如果下載的 SDK 包含 d3dx10 \_33.dll 和 d3dx10 \_34.dll，則隨附于該 sdk 的程式庫 (d3dx10) .lib 將載入 d3dx10 \_34.dll。 如果後續的 SDK 稍後再安裝包含 d3dx10 \_ 35... a sdk，則先前 sdk 的 d3dx10 仍會載入 d3dx10 \_34.dll。 較新 SDK 的 d3dx10 會載入 d3dx10 \_35.dll。

## <a name="redistributing-binaries"></a>轉散發二進位檔

您只能重新散發相同檔案) 的 d3dx10.dll (和後續版本。 若要重新發佈此檔案，您必須使用 **DirectXSetup** 函數。 如需使用此函式並將可轉散發套件放在一起的詳細資訊，請參閱使用 [DirectSetup 安裝 DirectX](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx)。 Windows Vista 中包含所有其他必要的二進位檔。 唯一可轉散發的二進位檔是位於下列目錄中的二進位檔。


```
(SDK root)\Redist
```



下表描述開發人員應該注意的二進位檔。



| Direct3D 10 二進位檔   | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | 零售和 debug D3DX10 元件;零售元件可以在可轉散發套件的封包中轉散發。                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | 參考轉譯器。 提供圖形管線的軟體執行。 只包含為 Windows SDK 或舊版 DirectX SDK 的一部分，而且無法重新散發。 參考轉譯器僅適用于偵錯工具。 不需要明確連結;嘗試建立參考設備 (請參閱 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) 將會載入此 dll （如果有的話）。                                                                                                    |
| d3d10sdklayers.dll     | 一系列的 SDK 公用程式，可做為 API 呼叫與執行時間執行之間的一層，包括 [debug 層](d3d10-graphics-programming-guide-api-features-layers.md) 和切換為參考層。 不需要明確連結;如果使用適當的圖層旗標建立裝置，則會自動載入此 DLL。 此元件僅供開發和偵測之用。 只包含為 Windows SDK 或舊版 DirectX SDK 的一部分，而且無法重新散發。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 10 程式設計手冊](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Direct3D 10 圖形](d3d10-graphics.md)
</dt> </dl>

 

 



