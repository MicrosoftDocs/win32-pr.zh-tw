---
description: 授權會設定您有權存取的資源。
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Web 網頁的授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141323"
---
# <a name="authorization-for-web-pages"></a>Web 網頁的授權

授權會設定您有權存取的資源。

**目標：** 允許使用者存取您的應用程式。

## <a name="prerequisites"></a>必要條件

無

**完成時間：** 2 分鐘。

## <a name="instructions"></a>指示

### <a name="1-authorization"></a>1. 授權

當使用者輸入其認證，並按一下 [登入] 按鈕時，會顯示 [許可權] 頁面。 此頁面最適合讓使用者控制授與應用程式存取 Contoso 資料的細微許可權。 ![contoso 許可權頁面](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. 如何使用範例

您必須知道下列 HTML 和 CSS 檔案。

1.  下列 HTML 檔案會對應至 web 授權流程中的兩個頁面
    -   WebAuthLogin.html-登入頁面的範例 HTML
    -   WebAuthPermissions.html-許可權頁面的範例 HTML
2.  CSS 檔案包含 Windows 8 的樣式，可協助您建立 Windows Store 應用程式網頁。
    -   ui-light-這是衍生自 Windows 8 控制項的基底樣式表單。
    -   ui-webauth：這會提供用於將 web 驗證頁面的版面配置優化的遞增樣式。
    -   theme-colors：這會提供遞增樣式，以使用提供者的品牌色彩覆寫控制項的預設輔色。

## <a name="summary-and-next-steps"></a>摘要和後續步驟

[驗證網頁的摘要教學](tutorial-for-authenticating-web-pages.md)課程

[設計驗證網頁的下一個最佳作法](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
