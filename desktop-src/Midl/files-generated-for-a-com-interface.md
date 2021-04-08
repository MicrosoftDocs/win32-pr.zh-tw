---
title: 針對 COM 介面產生的檔案
description: 針對 COM 介面，MIDL 編譯器會將所有用戶端和物件服務器輔助常式和資料結合成單一介面 proxy 檔案。
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL 編譯器 MIDL、MIDL 和 COM
- COM MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933163"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="7630b-105">針對 COM 介面產生的檔案</span><span class="sxs-lookup"><span data-stu-id="7630b-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="7630b-106">針對 COM 介面，MIDL 編譯器會將所有用戶端和物件服務器輔助常式和資料結合成單一介面 proxy 檔案。</span><span class="sxs-lookup"><span data-stu-id="7630b-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="7630b-107">此檔案包含用戶端和伺服器的代理進入點。</span><span class="sxs-lookup"><span data-stu-id="7630b-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="7630b-108">此外，MIDL 編譯器會產生介面標頭檔、介面 UUID 檔案和介面註冊檔案。</span><span class="sxs-lookup"><span data-stu-id="7630b-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="7630b-109">在建立包含程式碼的 proxy DLL 時，您將會使用這些檔案，以支援用戶端應用程式和物件服務器的介面使用。</span><span class="sxs-lookup"><span data-stu-id="7630b-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="7630b-110">當您為使用介面的用戶端應用程式建立可執行檔時，您也會使用介面標頭檔和介面 UUID 檔。</span><span class="sxs-lookup"><span data-stu-id="7630b-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="7630b-111">下列主題描述針對自訂 COM 介面產生的每個檔案，您可以 **\[** [](object.md) **\]** 在 IDL 檔案的介面屬性清單中包含物件屬性來識別這些檔案：</span><span class="sxs-lookup"><span data-stu-id="7630b-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="7630b-112">介面 Proxy 檔案</span><span class="sxs-lookup"><span data-stu-id="7630b-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="7630b-113">標頭檔</span><span class="sxs-lookup"><span data-stu-id="7630b-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="7630b-114">介面 UUID 檔案</span><span class="sxs-lookup"><span data-stu-id="7630b-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="7630b-115">介面註冊檔案</span><span class="sxs-lookup"><span data-stu-id="7630b-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="7630b-116">如需詳細資訊，請參閱 [應用程式佈建檔 (ACF)](application-configuration-file-acf-.md)、 [**/App \_ config**](-app-config.md)、 [介面定義 (IDL)](interface-definition-idl-file.md)檔案，以及 [建立和註冊 Proxy DLL](../com/building-and-registering-a-proxy-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="7630b-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 