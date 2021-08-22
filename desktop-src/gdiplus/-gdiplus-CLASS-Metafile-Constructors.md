---
description: 本主題列出中繼檔類別的函式。 如需完整的類別清單，請參閱中繼檔類別。
ms.assetid: a9648287-65d9-47d8-b32b-33f74b4fcd07
title: 中繼檔中繼檔
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9a993cb8d0e21e57fe495e5948546ab8ea51e2829af3bd42b962a0be9408e419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977848"
---
# <a name="metafilemetafile-constructors"></a>中繼檔中繼檔

本主題列出 [**中繼檔**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別的函式。 如需完整的類別清單，請參閱 **中繼檔類別**。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                                                                                                                      | 描述                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**中繼檔 (WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar))                                                                                                          | 建立用來播放的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar)) 物件。<br/>                                                                                                                                                   |
| [**中繼檔 (IStream \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))                                                                                                          | 從 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面建立用來播放的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))物件。<br/>                                                            |
| [**中繼檔 (HENHMETAFILE，BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool))                                                                                          | 根據 GDI 增強型中繼檔 (EMF) 檔，建立 GDI+ 的 [**中繼檔：：元**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool))檔物件以進行播放。<br/>                                                                                            |
| [**中繼檔 (HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar))                                                                         | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar)) 物件。<br/>                                                                                                                             |
| [**中繼檔 (WCHAR \* 、HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar))                                                        | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar)) 物件。<br/>                                                                                                                    |
| [**中繼檔 (IStream \* 、HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))                                                        | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))物件。<br/>                               |
| [**中繼檔 (HMETAFILE、WmfPlaceableFileHeader \* 、BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool))                                             | 建立 GDI+ 的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool))物件以進行錄製。 格式將會是可放置的中繼檔。<br/>                                                                          |
| [**中繼檔 (HDC、Rect&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))            | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (HDC、RectF&、MetaFileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))           | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (WCHAR \* 、HDC、Rect&、MetaFileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))    | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (WCHAR \* 、HDC、RectF&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))   | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (IStream \* 、HDC、Rect&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))  | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))物件。<br/> |
| [**中繼檔 (IStream \* 、HDC、RectF&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))物件。<br/> |



 

 
