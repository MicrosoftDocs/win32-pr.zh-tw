---
description: 您可以使用 Windows Installer 來偵測遺失的元件或檔案，然後重新安裝包含遺漏元件的功能。
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: 安裝遺失的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986884"
---
# <a name="installing-a-missing-component"></a>安裝遺失的元件

您可以使用 Windows Installer 來偵測遺失的元件或檔案，然後重新安裝包含遺漏元件的功能。 因為安裝程式會安裝功能，而不是元件，所以必須先解析遺失檔案所屬的元件，然後再安裝包含該元件的功能。 如果有一個以上的功能連結至元件，安裝程式會安裝需要最少磁碟空間的功能。

如果您呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)，您可以確認元件的金鑰檔是否存在。 不過，仍有可能遺失屬於元件的其他檔案。 在該案例中，請呼叫 [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)。 然後，安裝程式會解析為檔案所屬的元件，並安裝連結到需要最少磁碟空間之元件的功能。

如果 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函式意外失敗，您必須安裝任何遺失的元件。

下列程式說明如何安裝遺失的元件。

**偵測並安裝遺失的元件**

1.  呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 來確認元件的金鑰檔是否存在。 但是，即使元件的金鑰檔存在，仍然可能遺失屬於元件的其他檔案。
2.  如果與元件相關聯的功能未知，則呼叫 [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) 函數。
3.  如果已知與元件相關聯的功能，請呼叫 [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) 或 [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) 函數。
4.  如果應用程式無法開啟檔案，請呼叫 [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) 。

 

 



