---
description: 從檔案讀取現有的 CMC 憑證要求、將其包裝在另一個 CMC 要求中、簽署此外部要求、將它提交給憑證授權單位單位 (CA) ，然後將憑證回應儲存至檔案。
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882938"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

EnrollNestedCMC 範例會從檔案讀取現有的 CMC 憑證要求、將其包裝在另一個 CMC 要求中、簽署此外部要求、將它提交給憑證授權單位單位 (CA) ，然後將憑證回應儲存至檔案。

## <a name="location"></a>Location

當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，預設會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ X509 憑證註冊 \\ VC \\ enrollNestedCMC 資料夾中安裝範例。

## <a name="discussion"></a>討論

EnrollNestedCMC 範例：

1.  處理下列命令列引數：
    -   輸入檔的名稱。
    -   輸出檔的名稱。
    -   選用的要求範本。
2.  從檔案讀取現有的 CMC 要求作為 base63 編碼的位元組陣列、將位元組陣列轉換成 **BSTR**、建立 [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) 物件，並使用 **BSTR** 來初始化 request 物件。 初始化的物件會成為內部要求。
3.  使用在上一個步驟中建立並初始化的內部要求物件來初始化另一個 CMC 要求。
4.  抓取現有的簽署憑證，如果找不到，則會從命令列上指定的範本建立憑證要求，並嘗試進行註冊。 FindCertByTemplate 和 enrollCertByTemplate 函數是在 enrollCommon 中定義。
5.  從外部 CMC 要求抓取 [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) 集合、建立新的 [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) 物件、使用抓取的簽署憑證將它初始化，然後將它新增至集合。
6.  使用可辨別編碼規則 (DER) 來編碼 CMC 要求，並以 **BSTR** 形式抓取要求。
7.  建立 [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) 物件，並使用它來取出包含 CA 設定的字串。
8.  建立 CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) 物件，並使用它加上包含 ca 設定的字串，以及將要求提交到 ca 的憑證要求。
9.  檢查註冊程式的狀態，並將憑證回應從 CA 儲存至檔案。 EncodeToFileW 函式定義于 enrollCommon .cpp 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CMC 要求](cmc-request.md)
</dt> <dt>

[使用包含的範例](using-the-included-samples.md)
</dt> </dl>

 

 
