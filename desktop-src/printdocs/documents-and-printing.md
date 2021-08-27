---
description: 這些主題說明可讓應用程式儲存、觀看和列印 Windows 的檔和列印功能。
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 文件和列印
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472364"
---
# <a name="documents-and-printing"></a>文件和列印

這些主題說明可讓應用程式儲存、觀看和列印 Windows 的檔和列印功能。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">列印功能的新功能</a><br /> | Windows 8 支援使用<a href="/previous-versions/windows/apps/hh465225(v=win.10)">JavaScript 和 HTML 來列印 Windows store 應用程式</a>，以及<a href="/previous-versions/windows/apps/hh465196(v=win.10)">使用 c #/VB/c + + 和 XAML Windows store 應用程式的列印</a>。<br /> Windows 8 也包含新的 COM 型 API，可為 Open XPS 提供完整的支援，並可存取 Windows 8 支援的新印表機驅動程式部分。 如需新 API 的詳細資訊，請參閱 <a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案封裝 API</a>。<br /> Windows 列印驅動程式收件匣程式可確保 Windows 8 包含高百分比的熱門印表機支援。<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">XPS 文件</a><br /> | Xps 檔 API XPS 數位簽章的相關資訊。<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS 檔 API</a><br /> xps 檔 API 是支援 XPS OM 的原生 Windows API。 XPS 檔 API 是在 Windows 7 中引進，可用於使用者模式程式和 XPSDrv 印表機驅動程式。<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS 數位簽章 API</a><br /> XPS 數位簽章可啟用檔簽署、簽署簽署者的身分識別，以及指出 XPS 檔在簽署之後是否已經變更。<br /></li></ul> | 
| <a href="printdocs-printing.md">列印</a><br /> | Windows 所支援列印功能的相關資訊。 這些功能包括：<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案套件 API</a><br /> 為應用程式提供可讓您管理 <strong>PrintDocument</strong> 套件的介面。<br /></li><li><a href="print-spooler-api.md">列印多工緩衝處理器 API</a><br /> 提供列印多工緩衝處理器的介面，讓應用程式可以管理印表機和列印工作。<br /></li><li><a href="print-ticket-api.md">列印票證 API</a><br /> 為應用程式提供管理和轉換列印票證的功能。<br /></li><li><a href="gdi-printing.md">GDI 列印 API</a><br /> 提供應用程式與裝置無關的列印介面。 <br /></li><li><p><a href="xps-printing.md">XPS 列印 API</a><br /> 提供可讓應用程式用來將 XPS 檔傳送至印表機的列印多工緩衝處理器介面。</p><blockquote>[!Note]<br />XPS 列印 API 不受支援，未來可能會變更或無法使用。 用戶端應用程式應該改用 <a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案套件 API</a> 。</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">列印架構</a><br /> | 列印架構和相關技術描述印表機的功能，並指定檔列印喜好設定至印表機和觀看應用程式。 <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">列印架構規格</a>是可下載的檔，其中包含列印架構的相關資訊，以及如何在檔和列印中使用它。 本章節中所找到的線上資訊只提供給您的資訊，而且可能無法精確反映出目前版本的 <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">列印架構規格</a>。<br /> 如需最新的設計資訊，請參閱 <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">列印架構規格</a> 。<br /> | 




 

## <a name="additional-resources"></a>其他資源

[列印範例範例應用程式](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))示範如何從 Windows 8 開始，從 Windows Store 應用程式進行列印。

本節所述的功能適用于原生 Windows 程式設計。 若要在 .net (managed) 程式設計中使用類似的功能，請參閱[Windows Presentation Foundation 檔](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85))。

XPS 檔建基於 [封裝](/previous-versions/windows/desktop/opc/packaging) API。 請參閱封裝 API，以取得較低層級的 XPS 檔內容存取權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[雙向列印機通訊 (硬體開發人員中心) ](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
