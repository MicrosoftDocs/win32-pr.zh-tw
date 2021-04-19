---
description: Windows 為應用程式提供一組完整的功能，讓您可以列印至各種裝置，例如雷射印表機、向量繪圖器、點陣印表機和傳真電腦。
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: '列印 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974509"
---
# <a name="printing-documents-and-printing"></a>列印 (檔和列印) 

Windows 為應用程式提供一組完整的功能，讓您可以列印至各種裝置，例如雷射印表機、向量繪圖器、點陣印表機和傳真電腦。

## <a name="desktop-app-printing"></a>桌面應用程式列印

Windows 程式設計人員可以從數種不同的技術中進行選取，以從應用程式進行列印。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>技術</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案套件 API</a><br/></td>
<td>提供可讓應用程式存取和管理列印檔案封裝的介面。 此 API 適用于 Windows 8 和更新版本的 Windows。<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">列印多工緩衝處理器 API</a><br/></td>
<td>提供列印多工緩衝處理器的介面，讓應用程式可以管理印表機和列印工作。<br/> 應用程式會使用「列印 <a href="print-spooler-api.md">幕後處理</a> 程式」 api 來啟動、停止、控制及設定列印多工緩衝處理器所管理的列印工作，不論它們是使用 <a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案封裝 Api</a> 或 <a href="gdi-printing.md">GDI 列印 API</a> 來列印內容。<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">列印票證 API</a><br/></td>
<td>為應用程式提供管理和轉換列印票證的功能。<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">GDI 列印 API</a><br/></td>
<td>提供應用程式與裝置無關的列印介面。 <br/>
<blockquote>
[!Note]<br />
針對 Windows Vista 和更新版本的 Windows 撰寫應用程式的開發人員，應該考慮在應用程式中使用 <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS 檔 API</a> 。
</blockquote>
<br/> <a href="gdi-printing.md">GDI 列印 API</a>適用于必須在 windows XP 和較早版本的 windows 上執行的應用程式。<br/></td>
</tr>
</tbody>
</table>



 

下圖提供不同列印 Api 相關方式的高階觀點。

![顯示原生 windows 應用程式如何使用列印 api 的圖表](images/print-apis.png)

 

本節中的 [列印檔案套件 API](./tailored-app-printing-api.md)會說明您可以搭配 Windows 8 和更新版本的 Windows desktop 使用的列印檔案套件和預覽列印介面。

如需從以 JavaScript 和 HTML 撰寫的 Windows Store 應用程式進行列印的詳細資訊，請參閱 [使用 javascript 和 html) 列印 (Windows store 應用程式 ](/previous-versions/windows/apps/hh465225(v=win.10))。 如需從以 c #、Microsoft Visual Basic 或 c + + 和 XAML 撰寫的 Windows Store 應用程式進行列印的詳細資訊，請參閱 [使用 c) 列印 (Windows store 應用程式 ](/previous-versions/windows/apps/hh465196(v=win.10))。

> [!Note]  
> 如需可在 Windows Store 應用程式中使用的桌面應用程式列印 Api 清單，請參閱 [適用于 Windows store 應用程式的 Win32 和 COM (列印和檔) ](/uwp/win32-and-com/win32-and-com-for-uwp-apps) 。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[雙向列印機通訊 (硬體開發人員中心) ](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

