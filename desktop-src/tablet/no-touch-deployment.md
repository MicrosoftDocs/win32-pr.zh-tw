---
description: Microsoft .NET Framework 讓您能夠從 Web 或檔案伺服器部署應用程式。
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: 無觸控部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106981728"
---
# <a name="no-touch-deployment"></a>無觸控部署

Microsoft .NET Framework 讓您能夠從 Web 或檔案伺服器部署應用程式。 這項稱為「無接觸部署」的技術，結合智慧型用戶端應用程式的效能和互動功能與 Web 應用程式的所有部署優勢。 若要透過 Web 部署您的應用程式，請在包含可執行檔的資料夾上按一下滑鼠右鍵，然後選取 [ **屬性**]。 在 [ **Web 共用** ] 索引標籤上，選取 [ **共用這個資料夾**]。 輸入資料夾的別名。 現在，您可以使用該別名做為您伺服器上的目錄，在 Web 上執行可執行檔。 如需有關無接觸部署的詳細資訊，請參閱 .NET Framework 中的 [.Net 智慧型用戶端](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) 和 [無接觸部署](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)。

> [!Note]  
> 您必須在電腦上安裝 Microsoft Internet Information Services (IIS **) ，才能在 [內容**] 對話方塊中啟用 [ **Web 共用**] 索引標籤。

 

將不需要觸控的部署套用至啟用筆墨的應用程式，其方式與任何其他 Windows Forms 應用程式相同。 Microsoft Windows XP Tablet PC Edition 軟體發展工具組所提供的範例 (SDK) 包含自動宣告範例的無觸控部署版本，位於範例的筆墨 Web 範例一節中。 此範例會採用原始的 [自動宣告表單範例](auto-claims-form-sample.md) ，並提供在 Web 共用上放置的安裝程式。 當 Microsoft Internet Explorer 流覽至對應至 Web 共用的目錄中 AutoClaims.exe 時，就會啟動應用程式。 如需範例的詳細資訊，請參閱 [無觸控部署 Web 範例](no-touch-deployment-web-sample.md) 。

> [!Note]  
> 當您透過 Web 部署 .NET 應用程式時，應用程式可能會受到 .NET 安全性模型的影響。 [ [安全性與信任](security-and-trust.md) ] 區段說明安全性如何與啟用筆墨的 Web 應用程式搭配運作。

 

 

 