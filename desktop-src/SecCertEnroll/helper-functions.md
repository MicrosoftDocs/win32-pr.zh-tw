---
description: 下列各節將討論 Xenroll.dll 所匯出的函式。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: " (憑證註冊 API) 的 Helper 函式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99282099f93482e3064a00eed146464a8d537e70d803b3b51389f92d9f93912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669828"
---
# <a name="helper-functions-certificate-enrollment-api"></a> (憑證註冊 API) 的 Helper 函式

下列各節將討論 Xenroll.dll 所匯出的函式。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。

## <a name="binaryblobtostring"></a>binaryBlobToString

Xenroll.dll 中的 [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) 函數會將位元組陣列轉換成字串。

使用 CertEnroll.dll，您就可以在 [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)介面上呼叫 [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring)方法。

## <a name="stringtobinaryblob"></a>stringToBinaryBlob

Xenroll.dll 中的 [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) 函數會將字串轉換為位元組陣列。

使用 CertEnroll.dll，您就可以在 [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)介面上呼叫 [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray)方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
