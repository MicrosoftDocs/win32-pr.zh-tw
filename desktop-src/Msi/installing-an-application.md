---
description: 您可以使用 Windows Installer 的功能來安裝整個產品。 下列步驟說明如何安裝產品。
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: 安裝應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aad6e130d78bd30b940232aeb6fe1da6508be754fe50b9abb9dbcaa0186562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327958"
---
# <a name="installing-an-application"></a>安裝應用程式

您可以使用 Windows Installer 的功能來安裝整個產品。 下列步驟說明如何安裝產品。

**安裝產品**

1.  藉由呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 函式，透過其安裝或卸載循序執行產品。
2.  藉由呼叫 [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) 函數來指定安裝層級。

    您可以使用 [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) 函數的參數來設定安裝狀態。 例如，您可以設定要在本機安裝或從來源安裝的狀態。 您可以設定層級來設定要包含的產品功能範圍。

如需安裝應用程式的詳細資訊，請參閱 [復原](resiliency.md) 和 [安裝機制](installation-mechanism.md)。

 

 



