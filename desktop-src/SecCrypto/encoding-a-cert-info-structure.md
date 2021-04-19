---
description: 編碼程式是解碼憑證資訊結構中所述解碼程式的反向 \_ 。
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: 編碼 CERT_INFO 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975518"
---
# <a name="encoding-a-cert_info-structure"></a><span data-ttu-id="a3343-103">編碼 CERT \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="a3343-103">Encoding a CERT\_INFO Structure</span></span>

<span data-ttu-id="a3343-104">編碼程式是 [解碼憑證 \_ 資訊結構](decoding-a-cert-info-structure.md)中所述解碼程式的反向。</span><span class="sxs-lookup"><span data-stu-id="a3343-104">The encoding process is the reverse of the decoding process described in [Decoding a CERT\_INFO Structure](decoding-a-cert-info-structure.md).</span></span> <span data-ttu-id="a3343-105">例如，下列程式會將編碼的 **簽發者** 新增至 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="a3343-105">For example, the following procedure would add an encoded **Issuer** to a [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) structure.</span></span> <span data-ttu-id="a3343-106">另請參閱程式後面的圖例。</span><span class="sxs-lookup"><span data-stu-id="a3343-106">Also see the illustration that follows the procedure.</span></span>

<span data-ttu-id="a3343-107">**若要將編碼的簽發者加入 CERT \_ 資訊結構中**</span><span class="sxs-lookup"><span data-stu-id="a3343-107">**To add an encoded Issuer to a CERT\_INFO structure**</span></span>

1.  <span data-ttu-id="a3343-108">建立字串，其中包含要使用的簽發者名稱。</span><span class="sxs-lookup"><span data-stu-id="a3343-108">Create a string containing the issuer name to be used.</span></span>
2.  <span data-ttu-id="a3343-109">建立 [**CERT \_ RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構的陣列，此陣列將會初始化以包含剛剛建立之簽發者名稱字串的適當資訊。</span><span class="sxs-lookup"><span data-stu-id="a3343-109">Create an array of [**CERT\_RDN\_ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) structures, which will be initialized to contain the proper information about the issuer name string just created.</span></span>
3.  <span data-ttu-id="a3343-110">建立 [**cert \_ rdn**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) 結構的陣列，其中一個具有剛剛初始化之 [**cert \_ rdn \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) 結構陣列的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a3343-110">Create an array of [**CERT\_RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) structures, one of which has the information about the array of [**CERT\_RDN\_ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) structures just initialized.</span></span>
4.  <span data-ttu-id="a3343-111">建立具有剛剛建立之 [**cert \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn)結構陣列指標的 [**CERT \_ NAME \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info)結構。</span><span class="sxs-lookup"><span data-stu-id="a3343-111">Create a [**CERT\_NAME\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) structure that has a pointer to the array of [**CERT\_RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) structures that just created.</span></span>
5.  <span data-ttu-id="a3343-112">呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 以取得輸出編碼 BLOB 的大小，並將您剛才建立的憑證 [**\_ 名稱 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) 結構的位址傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="a3343-112">Call [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) to get the size of the output encoded BLOB, passing it the address of the [**CERT\_NAME\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) structure that you just created.</span></span>
6.  <span data-ttu-id="a3343-113">配置輸出編碼 BLOB 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a3343-113">Allocate memory for the output encoded BLOB.</span></span>
7.  <span data-ttu-id="a3343-114">再次呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ，將相同的資訊傳遞給它，但現在會將剛剛配置的記憶體位址傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="a3343-114">Call [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) again, passing it the same information, but now passing it the address of the memory just allocated.</span></span>
8.  <span data-ttu-id="a3343-115">將 [**CERT \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構的 **cbData** 成員設定為步驟5中所傳回的大小，並將 **>pbdata** 成員設定為步驟6中所取得的位址。</span><span class="sxs-lookup"><span data-stu-id="a3343-115">Set the **Issuer.cbData** member of the [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) structure to the size returned in step 5, and the **Issuer.pbData** member to the address obtained in step 6.</span></span> <span data-ttu-id="a3343-116">編碼的 **簽發者** BLOB 現在位於該處。</span><span class="sxs-lookup"><span data-stu-id="a3343-116">The encoded **Issuer** BLOB now resides there.</span></span>

![將編碼的簽發者加入 cert \- 資訊結構中](images/encflow.png)

<span data-ttu-id="a3343-118">若要初始化及編碼某些憑證延伸資訊，請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="a3343-118">To initialize and encode some certificate extension information, use the following procedure.</span></span> <span data-ttu-id="a3343-119">另請參閱程式後面的圖例。</span><span class="sxs-lookup"><span data-stu-id="a3343-119">Also see the illustration that follows the procedure.</span></span>

<span data-ttu-id="a3343-120">**若要將編碼的延伸模組資訊新增至 CERT \_ 資訊結構**</span><span class="sxs-lookup"><span data-stu-id="a3343-120">**To add encoded extension information to a CERT\_INFO structure**</span></span>

1.  <span data-ttu-id="a3343-121">建立並初始化延伸模組資訊結構，在此範例中，它是 [**CERT \_ BASIC \_ 條件約束 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="a3343-121">Create and initialize an extension information structure—for this example, it is a [**CERT\_BASIC\_CONSTRAINTS\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) structure.</span></span>
2.  <span data-ttu-id="a3343-122">呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)，並將剛才建立的結構位址傳遞給它，以取得輸出編碼 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="a3343-122">Call [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), passing it the address of the structure just created, to get the size of the output encoded BLOB.</span></span>
3.  <span data-ttu-id="a3343-123">配置輸出編碼 BLOB 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a3343-123">Allocate memory for the output encoded BLOB.</span></span>
4.  <span data-ttu-id="a3343-124">再次呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 並傳遞相同的資訊，但現在會傳入所配置記憶體的位址。</span><span class="sxs-lookup"><span data-stu-id="a3343-124">Call [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) again, passing the same information, except now pass in the address of the allocated memory.</span></span>
5.  <span data-ttu-id="a3343-125">建立 [**CERT \_ 擴充**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="a3343-125">Create an array of [**CERT\_EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) structures.</span></span>
6.  <span data-ttu-id="a3343-126">初始化其中一個憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) 結構，讓 **pszObjId** 是 **值** 中所含資料的適當字串 **，而該值包含從** 呼叫 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)輸出的加密資料 BLOB。</span><span class="sxs-lookup"><span data-stu-id="a3343-126">Initialize one of the [**CERT\_EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) structures so that the **pszObjId** is the proper string for the data contained in **Value**, and that **Value** contains the encrypted data BLOB that was output from the call to [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).</span></span>
7.  <span data-ttu-id="a3343-127">初始化 [**cert \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)結構的 **rgExtension** 成員，以指向憑證 [**\_ 延伸**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="a3343-127">Initialize the **rgExtension** member of the [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) structure to point to the array of [**CERT\_EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) structures.</span></span>

![將編碼的延伸模組資訊新增至 cert \- 資訊結構](images/xtenflow.png)

 

 



