---
description: 下列各節會討論 Xenroll.dll 所匯出的函式，以 Exchange (PFX) 訊息來管理個人資訊。
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: 個人資訊 Exchange 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e7cddcda00131b64c5fe6122d777695bbab4f80cbac8e71648a2197fed036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774681"
---
# <a name="personal-information-exchange-functions"></a>個人資訊 Exchange 功能

下列各節會討論 Xenroll.dll 所匯出的函式，以 Exchange (PFX) 訊息來管理個人資訊。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。

## <a name="createfilepfxwstr"></a>createFilePFXWStr

Xenroll.dll 中的 [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) 函數會使用 PFX 格式，將憑證鏈和 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 儲存在檔案中。

CertEnroll.dll 程式庫不會直接執行將 PFX 訊息複製到檔案的功能。 不過，您可以使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)介面上的 [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法來建立已編碼的 PFX 訊息，並撰寫自訂函式，以將訊息儲存在檔案中。

## <a name="createpfxwstr"></a>createPFXWStr

Xenroll.dll 中的 [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) 函式會以 PFX 格式字串儲存憑證鏈和私密金鑰。

您可以使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)介面上的 [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法來建立編碼的 PFX 訊息，其中包含憑證鏈和金鑰。 您可以指定密碼、匯出選項和編碼類型。 若要取出相當於 [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)所傳回的字串，請在 \_ \_ \_ [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法的 *編碼* 參數中傳遞 XCN CRYPT 字串二進位旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
