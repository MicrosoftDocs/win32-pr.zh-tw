---
title: Windows動畫範例
description: 本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows動畫 Windows 動畫、範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9119ab7333f1f5d74b9be9998ad26b36139f9a92d88fec856d3f4572d12f431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656148"
---
# <a name="windows-animation-samples"></a>Windows動畫範例

本節所包含的主題會提供支援 Windows 動畫管理員檔的程式碼範例詳細資料。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                     | 描述                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [應用程式驅動的動畫範例](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [計時器驅動動畫範例](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [自訂插即用範例](custom-interpolator-sample.md)<br/>                   | 示範如何搭配使用 Windows 動畫與您自己的自訂插即用來呈現 Direct2D。 <br/> |
| [方格版面配置範例](grid-layout-sample.md)<br/>                                   | 示範如何使用 Direct2D 以動畫顯示影像的格線，以使用 Windows 動畫。 <br/>                         |
| [優先順序比較範例](priority-comparison-sample.md)<br/>                   | 示範如何使用 Direct2D 進行轉譯，以搭配您自己的優先順序比較來使用 Windows 動畫。<br/>      |



 

## <a name="sample-files"></a>範例檔案

每個範例都包含下列許多金鑰檔：

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>應用程式 .cpp
</dt> <dd>

定義應用程式進入點。

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow。h
</dt> <dd>

宣告 CMainWindow 類別。

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow .cpp
</dt> <dd>

初始化動畫元件和圖形平台、載入影像，以及呈現工作區。

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager。h
</dt> <dd>

宣告 CLayoutManager 類別。

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager .cpp
</dt> <dd>

在主視窗中計算影像的版面配置、建立分鏡腳本、將轉換新增至分鏡腳本，以及排定分鏡腳本。

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>縮圖。h
</dt> <dd>

宣告 CThumbNail 類別。

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>縮圖 .cpp
</dt> <dd>

建立動畫變數並呈現縮圖。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows動畫開發指南](windows-animation-developer-guide.md)
</dt> <dt>

[Windows動畫參考](windows-animation-reference.md)
</dt> </dl>

 

 





