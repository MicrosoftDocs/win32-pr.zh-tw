---
description: 本主題列出中繼檔類別的函式。 如需完整的類別清單，請參閱中繼檔類別。
ms.assetid: a9648287-65d9-47d8-b32b-33f74b4fcd07
title: 中繼檔中繼檔
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9ae5fa3343aebace286591760a47a55fbbef7c9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319024"
---
# <a name="metafilemetafile-constructors"></a>中繼檔中繼檔

本主題列出 [**中繼檔**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別的函式。 如需完整的類別清單，請參閱 **中繼檔類別**。

### <a name="overload-list"></a>多載清單



| 建構函式                                                                                                                                                                      | 描述                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**中繼檔 (WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar))                                                                                                          | 建立用來播放的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar)) 物件。<br/>                                                                                                                                                   |
| [**中繼檔 (IStream \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))                                                                                                          | 從 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面建立用來播放的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))物件。<br/>                                                            |
| [**中繼檔 (HENHMETAFILE，BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool))                                                                                          | 建立 GDI + [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool)) 物件，以根據 GDI 增強型中繼檔 (EMF) 檔播放。<br/>                                                                                            |
| [**中繼檔 (HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar))                                                                         | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar)) 物件。<br/>                                                                                                                             |
| [**中繼檔 (WCHAR \* 、HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar))                                                        | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar)) 物件。<br/>                                                                                                                    |
| [**中繼檔 (IStream \* 、HDC、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))                                                        | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))物件。<br/>                               |
| [**中繼檔 (HMETAFILE、WmfPlaceableFileHeader \* 、BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool))                                             | 建立要錄製的 GDI +[**中繼檔：：元**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool)) 檔物件。 格式將會是可放置的中繼檔。<br/>                                                                          |
| [**中繼檔 (HDC、Rect&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))            | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (HDC、RectF&、MetaFileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))           | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (WCHAR \* 、HDC、Rect&、MetaFileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))    | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (WCHAR \* 、HDC、RectF&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))   | 建立要錄製的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) 物件。<br/>                                                                                        |
| [**中繼檔 (IStream \* 、HDC、Rect&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))  | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))物件。<br/> |
| [**中繼檔 (IStream \* 、HDC、RectF&、MetafileFrameUnit、EmfType、WCHAR \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) | 建立用來錄製至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)介面的 [**中繼檔：：中繼檔**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))物件。<br/> |



 

 
