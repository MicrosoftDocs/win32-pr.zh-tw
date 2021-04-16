---
title: 'DirectWrite (DWrite) '
description: 現今的應用程式必須支援高品質的文字轉譯、解析度無關的大綱字型，以及完整的 Unicode 文字和版面配置支援。 DirectWrite 是 [DirectX](../directx.md) API，可提供這些功能和其他功能。
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2020
ms.locfileid: "104464173"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite) 

## <a name="purpose"></a>目的

現今的應用程式必須支援高品質的文字轉譯、解析度無關的大綱字型，以及完整的 Unicode 文字和版面配置支援。 DirectWrite 是 [DirectX](../directx.md) API，可提供這些功能和其他功能。

- 與裝置無關的文字版面配置系統，可改善檔和 UI 中的文字可讀性。
- 可使用[GDI](interoperating-with-gdi.md)、 [Direct2D](rendering-by-using-direct2d.md)或應用程式特定轉譯技術的高品質、子圖元、 [Microsoft ClearType](/typography/cleartype/)文字轉譯。
- 與 [Direct2D](rendering-by-using-direct2d.md)搭配使用時，硬體加速文字。
- 支援多重格式的文字。
- 支援 OpenType 字型的先進印刷樣式功能。
- 支援所有支援語言的文字版面配置和轉譯。
- [GDI](interoperating-with-gdi.md)相容的版面配置和轉譯。

API 支援測量、繪製和點擊測試多重格式的文字。 DirectWrite 會以 Windows 7 中的主要語言基礎結構為基礎，處理全球和當地語系化應用程式的所有支援語言文字。 DirectWrite 也提供低階字符轉譯 API，適用於想要執行自己的版面配置和 Unicode 對字符處理的開發人員。

> [!NOTE]
> [Project 留尼旺島](/windows/apps/project-reunion/) 導入了新版本的 DirectWrite， &mdash; 稱為 DWriteCore &mdash; ，可在 Windows 版本下執行以 Windows 8，並開啟您在跨平臺使用的大門。 如需詳細資訊，請參閱 [DWriteCore 總覽](dwritecore-overview.md)。

## <a name="run-time-requirements"></a>執行階段需求求

- Windows 7 或 Windows Vista Service Pack 2 (SP2) 和 Windows Vista 的平臺更新
- Windows Server 2008 R2 或 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 的平臺更新

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [DirectWrite 的新功能](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | 以下是一些 DirectWrite 新增專案。 <br/> |
| [程式設計指南](programming-guide.md)<br/> | 下列主題提供 DirectWrite API 的總覽。<br/> |
| [API 參考](reference.md)<br/> | 描述 DirectWrite API。<br/> |
| [範例程式碼](samples.md)<br/> | 本節包含 DirectWrite 範例程式的相關資訊。<br/> |
