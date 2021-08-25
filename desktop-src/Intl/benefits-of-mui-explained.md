---
description: MUI 的優點說明
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: MUI 的優點說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829697"
---
# <a name="benefits-of-mui-explained"></a>MUI 的優點說明

-   [適用于開發人員的 MUI 權益](#mui-benefits-for-developers)
-   [企業適用的 MUI 權益](#mui-benefits-for-enterprises)
-   [適用于 Oem 的 MUI 權益](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>適用于開發人員的 MUI 權益

有許多可能的方法可以在應用程式中執行 MUI 解決方案，但每個可能性都是三種基本方法之一的變化：

1.  使用內建資源編譯一個二進位 (，) 適用于每種語言。 這是繼承應用程式的 *事實上* 標準，因為這是標準開發工具（例如 Microsoft Visual Studio）所支援的主要模型。 此模型確實需要多個語言的多個二進位檔，並在單一映射部署和多語言案例方面有一些限制。 請注意，使用此模型開發的應用程式將繼續在 Windows Vista 上運作，而提供的工具可協助開發人員從這個模型移到第三種方法中所述的現代化模型。
2.  具有一個語言中立的核心二進位檔，其中有一個多語言資源動態連結程式庫 (DLL) 。 這種模型肯定是方便 MUI，但很難更新資源二進位檔以容納新的語言。 假設除了英文、法文和日文之外，您也想要支援德文。 您必須提供整個新的資源二進位檔，並將其部署給可能不需要德文的使用者。
3.  具有一個語言中立的核心二進位檔，每種語言都有一組資源 Dll。 這是作業系統本身在 Windows Vista 中的執行方式，而開發人員則建議將此模型用於應用程式，因為它提供的是上述兩個模型。

在 Windows Vista 發行之前，缺乏此第二個模型的內建支援，使其難以採用。 不過，這已經改變，而此模型的優點很多，因此成為應用程式的絕佳模型：

-   您可以使用與 Windows Vista 相同的方式，讓應用程式進行多語言的行為，並為使用者提供一致的顯示語言體驗。
-   在發行應用程式的其他語言時，會增加彈性。 其他語言可以與核心程式代碼分開發行，這表示您可以視需要在一段時間內加入新語言的支援。
-   在建立和維護更多語言版本時，會降低成本。
-   Oem 和企業可以輕鬆地將應用程式整合到他們的全球化電腦影像中，以便寄送至不同的國家/地區。
-   可使用的工具和指導方針可協助您將應用程式遷移至 Windows Vista MUI 模型。 特別是，MSDN 在 MUI 上提供一 [組重要的檔集](multilingual-user-interface.md) 。

## <a name="mui-benefits-for-enterprises"></a>企業適用的 MUI 權益

MUI 為企業提供兩大優點：

-   單一映射安裝： MUI 可讓企業使用單一安裝來推出、支援及維護相同的全球 (或) 映射的任何部分。 WindowsVista 擴充了作業系統的單一映射推出，因此商務應用程式也可以部署為相同映射的一部分。
-   多語系桌面的支援：多個當地語系化的 UI 語言套件可以安裝在桌面上，讓多個使用者可以共用單一桌面，同時仍使用自己慣用的 UI 語言。 這也適用于需要對所有正式語音 (語言進行同等處理的公用電腦，例如在加拿大和歐盟) ，以及將電腦用於漫遊使用者的情況下。

## <a name="mui-benefits-for-oems"></a>適用于 Oem 的 MUI 權益

Oem 的主要優點是 MUI 啟用的單一映射安裝，因為它可讓您建立包含所有必要語言的映射，以便有效地將目標設為地理區域，以及將語言選擇延遲到使用者的初始安裝電腦上。 特別是，這可讓您更有效地管理 Oem 的清查。

藉由提供應用程式的 MUI 支援，Windows Vista 也可讓 oem 在其映射上提供加值應用程式，同時從單一映射安裝獲益，只要這些應用程式已啟用 MUI 即可。

 

 



