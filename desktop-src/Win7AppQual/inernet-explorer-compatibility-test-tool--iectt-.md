---
description: .
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer 相容性測試工具 (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25e39263f448c7e11db1be32463b3801e4a8761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984554"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Internet Explorer 相容性測試工具 (IECTT)

Internet Explorer 相容性測試控管 (IECTT) 是 [Microsoft 應用程式相容性](/windows-hardware/get-started/adk-install)工具組的元件。 這項工具可協助您診斷 web 應用程式中的問題，方法是即時顯示問題，並選擇性地將結果上傳至 ACT 資料庫。 結果包括有關可能的相容性問題的詳細資料，以及有關每個相容性問題的詳細資訊連結。 IECTT 也可讓您排除問題和修改可用的屬性。

## <a name="to-open-iectt"></a>開啟 IECTT

1.  安裝 [Microsoft 應用程式相容性工具](/windows-hardware/get-started/adk-install)組。
2.  按一下 [ **開始**]，依序指向 [ **程式**]、[ **Microsoft 應用程式相容性** 工具組 5.6]、[ **開發人員和測試人員工具**]，然後按一下 [ **Internet Explorer 相容性測試控管**]。

下列各節說明常見的 IECTT 案例。

## <a name="view-issues-in-real-time"></a>即時查看問題

當您針對 Windows Internet Explorer 7 和 Windows Internet Explorer 8 測試網站和 web 應用程式時，可以即時找出並查看您的 web 架構問題。 完成測試之後，您可以在 IECTT 的 [ **即時資料** ] 畫面中查看結果。

## <a name="upload-issues-to-your-act-database"></a>將問題上傳至您的 ACT 資料庫

您可以將 web 式問題上傳至 ACT 資料庫，此資料庫會處理資訊，並可讓您在應用程式相容性管理員的 [ **分析** ] 畫面上查看結果。

## <a name="collect-your-compatibility-data"></a>收集您的相容性資料

您可以使用 Internet Explorer 7 或 Internet Explorer 7 的 IECTT 工具，收集您的網站和 web 應用程式相關的相容性資料。

**收集相容性資料**

1.  關閉所有作用中的 Windows Internet Explorer 視窗。
2.  在 IECTT 的 [ **Internet Explorer 相容性測試] 工具** 工具列上，按一下 [ **啟用**]。
3.  開啟 Internet Explorer 7 或 Internet Explorer 8] 視窗。

    此時會出現一則訊息，指出相容性評估記錄已開啟。

4.  造訪您的組織所需的網站或 web 應用程式。 當您造訪每個網站時，IECTT 工具會即時顯示您可能的相容性問題。
5.  在 [ **Internet Explorer 相容性測試控管** ] 工具列上，按一下 [ **停** 用] （當您完成時）。

    相容性記錄程式完成並停止。

## <a name="filter-your-issue-results"></a>篩選您的問題結果

您可以依物件名稱、問題類型或兩者來篩選任何 IECTT 結果。

**篩選您的問題結果**

1.  在 [ **Internet Explorer 相容性測試] 工具** 畫面上，按一下 [ **篩選**]。

    [ **問題篩選器** ] 對話方塊隨即出現。

2.  在 [ **輸入物件名稱來查看** box 的問題] 中，輸入您想要查看的物件名稱。

如需此工具和其他開發人員工具的詳細資訊，請參閱 MSDN Library 中的 [Internet Explorer 相容性測試控管是什麼？](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) 以及 IE8 blog 文章 [中的應用程式相容性記錄](/archive/blogs/ie/application-compatibility-logging-in-ie8) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用於調試 Web 應用程式和附加元件的工具](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
