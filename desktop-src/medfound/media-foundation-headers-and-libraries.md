---
description: 本主題列出定義所有媒體基礎 Api 的標頭和程式庫。
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: 媒體基礎的標頭和程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d5412f3f306c6e0d7327c1da1eb4c48bb109a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992523"
---
# <a name="media-foundation-headers-and-libraries"></a>媒體基礎的標頭和程式庫

本主題列出定義所有媒體基礎 Api 的標頭和程式庫。

若要尋找特定 API 元素的標頭和程式庫，請參閱 [媒體基礎程式設計參考](media-foundation-programming-reference.md)中的參考頁面。

## <a name="headers"></a>標題

-   codecapi。h
-   d3d11。h
-   d3d9。h
-   d3d9caps。h
-   d3d9types。h
-   dxva。h
-   dxva2api。h
-   dxvahd。h
-   evr。h
-   evr9。h
-   mfapi。h
-   mfcaptureengine. h
-   mferrors。h
-   mfidl。h
-   mfmediacapture。h
-   mfmediaengine。h
-   mfmp2dlna。h
-   mfobjects。h
-   mfplat .lib
-   mfplay。h
-   mfreadwrite。h
-   mftransform。h
-   opmapi。h
-   wmcodecdsp。h
-   wmcontainer。h

## <a name="libraries"></a>程式庫

-   dxva2 .lib
-   evr .lib
-   mf .lib
-   mfplat .lib
-   mfplay .lib
-   mfreadwrite .lib
-   mfuuid .lib

## <a name="library-changes-in-windows-7"></a>Windows 7 中的程式庫變更

從 Windows 7 開始，某些媒體基礎函數會從與舊版不同的 DLL 檔案匯出。

這些變更會影響下列 .lib 檔案：

-   evr .lib
-   mf .lib
-   mfplat .lib

使用任何這些函式的應用程式必須連結至不同的 .lib 檔案集，視 SDK 版本和目標平臺而定。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SDK 版本</th>
<th>程式庫</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>適用于 Windows Vista 的 Windows SDK<br/> 適用于 Windows Server 2008 的 Windows SDK<br/></td>
<td>evr .lib<br/> mf .lib<br/> mfplat .lib<br/></td>
</tr>
<tr class="even">
<td>適用于 Windows 7 的 Windows SDK</td>
<td>如果目標平臺是 Windows Vista 或 Windows Server 2008，請連結下列程式庫：<br/>
<ul>
<li>evr_vista .lib</li>
<li>mf_vista .lib</li>
<li>mfplat_vista .lib</li>
</ul>
如果目標平臺是 Windows 7 或更新版本，請連結下列程式庫：<br/>
<ul>
<li>evr .lib</li>
<li>mf .lib</li>
<li>mfplat .lib</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="additional-info-on-helper-functions"></a>Helper 函式的其他資訊

Windows 8 的 MFPlat.dll 是 Microsoft Windows 作業系統的元件。 它有數個包含在課程模組中的函式。

MFPlat 可針對低層級的記憶體配置、作業排程 FIFOs 和 win32 檔案存取抽象概念來實行 helper 功能。 為了更明確，它會提供下列支援：

-   配置和初始化記憶體緩衝區 (稱為「範例」 ) 和協助程式簡化管理其存留期
-   記憶體緩衝區的有效率資料複製功能
-   配置和初始化 operation FIFOs (稱為「事件」 ) 
-   執行簡單的時鐘物件
-   執行 win32 檔案包裝函式
-   配置和初始化 Cpu 和 Gpu 的記憶體緩衝區陣列

如果 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 方法成功，MFPlat 會提供下列工作佇列功能：

-   在內部支援 i/o 專案 (如 win32 檔案包裝函式和通訊端程式庫所使用) 
-   提供執行緒優先支援的多執行緒工作佇列陣列
-   透過工作佇列支援工作專案、計時器專案和等候專案

MFPlat 提供協助程式功能，可用於尋找和建立在系統上註冊的媒體轉換和媒體來源，以及建立和操作媒體類型，但 MFPlat 本身無法建立實際媒體，也無法播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




