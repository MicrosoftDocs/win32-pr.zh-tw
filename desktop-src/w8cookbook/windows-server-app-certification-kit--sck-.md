---
title: Microsoft 平臺就緒測試控管
description: Microsoft 平臺就緒測試控管
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683214"
---
# <a name="microsoft-platform-ready-test-tool"></a>Microsoft 平臺就緒測試控管

## <a name="platform"></a>平台

 **伺服器** – windows server 2012 \| Windows server 2012 R2  

## <a name="description"></a>Description

Microsoft Platform Ready (MPR) 測試控管可用於平臺應用程式的就緒程度，以及驗證 Windows Server 2012 和 Windows Server 2012 R2 應用程式的認證需求是否符合規範。

Microsoft 強烈建議您將 MPR 測試控管併入軟體組建和測試程式中，藉此確保在應用程式發行到市場之前，平臺已做好準備。 MPR 測試控管也是建議的工具，用來測試企業營運應用程式，以及評估伺服器產品的平臺相容性，然後再進行購買決策。

## <a name="requirements"></a>規格需求

MPR 測試控管包含的自動化測試：

-   Windows Installer
-   設定和主要功能
-   驅動程式和安全性
-   最佳做法

針對大部分的伺服器應用程式，自行測試及提交結果應該花費2小時或更少的時間。更複雜的應用程式可能需要大約4小時的時間。

所有驅動程式必須個別通過 Windows 硬體認證測試，並由 Microsoft 為 Windows Server 2012 進行簽署。

## <a name="usage"></a>使用方式

若要測試您的應用程式：

1.  安裝最新的 Windows Server 2012 最小設定 (完整伺服器 GUI、基本伺服器介面或 Server Core) ，視您的應用程式需求而來。
2.  檢查認證需求。
3.  在乾淨的系統上，以完整的 UI 模式或命令列模式執行 MPR 測試控管。
4.  完成自我引導的測試程式。
5.  查看結果，並視需要修正您的應用程式。
6.  登入，並將成功的結果上傳至 Microsoft Platform Ready 入口網站，以在標誌的 Windows Server Catalog 和使用中列出。

## <a name="resources"></a>資源

-   [Windows Server 應用程式認證方案的需求](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [Microsoft Platform Ready (MPR) 測試控管](https://www.microsoft.com/download/details.aspx?id=37143)
-   [Windows Server 2012 應用程式認證計畫](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [Windows Server 標誌意見反應](mailto:WSLogoFB@microsoft.com)

 

 