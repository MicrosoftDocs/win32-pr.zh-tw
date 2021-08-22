---
description: Windows安裝程式可以使用數位簽章來偵測損毀的資源。
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: 數位簽章和外部封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40edd8527eb93a6b970b3a8ce18fec8cc81f4688804a4e18f7ec5cdd748f3eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947462"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>數位簽章和外部封包檔

Windows安裝程式可以使用數位簽章來偵測損毀的資源。 安裝外部資源時，可能會根據在封裝中撰寫的參考簽署者憑證來驗證屬於資源的簽署者憑證。 安裝程式無法驗證內部封包的簽章。 它只能使用 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)來驗證數位簽章。

Windows安裝程式會在安裝儲存在外部封包中的檔案時執行下列動作：

-   安裝程式會檢查該外部封包的媒體專案是否列在 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)中。 儲存在外部封包中的檔案，其識別方式是在 [媒體資料表](media-table.md) 的 [封包] 資料行中，以 ' \# ' 字元為開頭的專案。
-   開啟外部封包之前，安裝程式會呼叫 WinVerifyTrust 以解壓縮目前的憑證和雜湊資訊。 如果封包上目前的簽章資訊與封裝中撰寫的簽章資訊不相符，則安裝會失敗。 安裝失敗，因為封包可能已遭入侵且無法信任。

如需有關使用數位簽章、數位憑證和 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)的詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的 [安全性](https://msdn.microsoft.com/library/cc527452.aspx)一節。

如需詳細資訊，請參閱 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)、 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)和 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)。

 

 
