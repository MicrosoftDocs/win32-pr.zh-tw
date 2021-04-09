---
description: Product 資料庫包含產品的相關資訊。 如需使用列舉函數取得產品資訊的詳細資訊，請參閱初始化應用程式。
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: 取得應用程式資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943765"
---
# <a name="getting-application-information"></a>取得應用程式資訊

Product 資料庫包含產品的相關資訊。 如需使用列舉函數取得產品資訊的詳細資訊，請參閱 [初始化應用程式](initializing-an-application.md)。

**取得產品資訊**

1.  藉由呼叫 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) 函式，確認是否已安裝產品。
2.  開啟資料庫，然後藉由呼叫 [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) 函數來取得其控制碼。

    如果資料庫包含在安裝封裝中，請呼叫 [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) 函數。

3.  使用開啟控制碼來取得具有 [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) 函式的產品屬性，並使用 [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) 函式取得描述性的功能資訊。

    如果您想要使用產品代碼取得產品資訊，而不是使用開放式資料庫控制碼，請呼叫 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) 函式，而不是 [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)。

4.  藉由呼叫 [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) 函數來關閉開啟的安裝控制碼。

    [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles)函式是診斷函數，不應該用來關閉您知道要開啟的控制碼。 當應用程式關閉時，可以接受呼叫 **MsiCloseAllHandles** 函式，以確保已關閉所有控制碼。

 

 



