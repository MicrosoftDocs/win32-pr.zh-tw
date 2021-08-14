---
description: 編碼程式是解碼憑證資訊結構中所述解碼程式的反向 \_ 。
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: 編碼 CERT_INFO 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b469ae0bdf02ffd8f30f8b0c2dd44051239a5702ff32704d58de8b60f1ca9701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766779"
---
# <a name="encoding-a-cert_info-structure"></a>編碼 CERT \_ 資訊結構

編碼程式是 [解碼憑證 \_ 資訊結構](decoding-a-cert-info-structure.md)中所述解碼程式的反向。 例如，下列程式會將編碼的 **簽發者** 新增至 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 結構。 另請參閱程式後面的圖例。

**若要將編碼的簽發者加入 CERT \_ 資訊結構中**

1.  建立字串，其中包含要使用的簽發者名稱。
2.  建立 [**CERT \_ RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構的陣列，此陣列將會初始化以包含剛剛建立之簽發者名稱字串的適當資訊。
3.  建立 [**cert \_ rdn**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) 結構的陣列，其中一個具有剛剛初始化之 [**cert \_ rdn \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構陣列的相關資訊。
4.  建立具有剛剛建立之 [**cert \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn)結構陣列指標的 [**CERT \_ NAME \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info)結構。
5.  呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 以取得輸出編碼 BLOB 的大小，並將您剛才建立的憑證 [**\_ 名稱 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) 結構的位址傳遞給它。
6.  配置輸出編碼 BLOB 的記憶體。
7.  再次呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ，將相同的資訊傳遞給它，但現在會將剛剛配置的記憶體位址傳遞給它。
8.  將 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構的 **cbData** 成員設定為步驟5中所傳回的大小，並將 **>pbdata** 成員設定為步驟6中所取得的位址。 編碼的 **簽發者** BLOB 現在位於該處。

![將編碼的簽發者加入 cert \- 資訊結構中](images/encflow.png)

若要初始化及編碼某些憑證延伸資訊，請使用下列程式。 另請參閱程式後面的圖例。

**若要將編碼的延伸模組資訊新增至 CERT \_ 資訊結構**

1.  建立並初始化延伸模組資訊結構，在此範例中，它是 [**CERT \_ BASIC \_ 條件約束 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) 結構。
2.  呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)，並將剛才建立的結構位址傳遞給它，以取得輸出編碼 BLOB 的大小。
3.  配置輸出編碼 BLOB 的記憶體。
4.  再次呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 並傳遞相同的資訊，但現在會傳入所配置記憶體的位址。
5.  建立 [**CERT \_ 擴充**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構的陣列。
6.  初始化其中一個憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構，讓 **pszObjId** 是 **值** 中所含資料的適當字串 **，而該值包含從** 呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)輸出的加密資料 BLOB。
7.  初始化 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構的 **rgExtension** 成員，以指向憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)結構的陣列。

![將編碼的延伸模組資訊新增至 cert \- 資訊結構](images/xtenflow.png)

 

 



