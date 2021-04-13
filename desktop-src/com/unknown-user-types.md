---
title: 未知的使用者類型
description: 未知的使用者類型
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316576"
---
# <a name="unknown-user-types"></a><span data-ttu-id="90c81-103">未知的使用者類型</span><span class="sxs-lookup"><span data-stu-id="90c81-103">Unknown User Types</span></span>

<span data-ttu-id="90c81-104">您可以藉由新增下列登錄機碼來簡化產品當地語系化：</span><span class="sxs-lookup"><span data-stu-id="90c81-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="90c81-105">**HKEY \_本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*</span><span class="sxs-lookup"><span data-stu-id="90c81-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="90c81-106">此索引鍵可讓函式傳回指定的字串，而不是預設值 "Unknown"，讓當地語系化人員指定不同語言的使用者類型。</span><span class="sxs-lookup"><span data-stu-id="90c81-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="90c81-107">COM 預設處理常式的 [**IOleObject：： GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) 執行會藉由呼叫 [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)來檢查登錄。</span><span class="sxs-lookup"><span data-stu-id="90c81-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="90c81-108">如果在登錄中找不到物件的類別，則會傳回物件之 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 實例的使用者類型。</span><span class="sxs-lookup"><span data-stu-id="90c81-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="90c81-109">如果在物件的 **IStorage** 實例中找不到類別，則會傳回字串 "Unknown"。</span><span class="sxs-lookup"><span data-stu-id="90c81-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90c81-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="90c81-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c81-111">註冊 COM 應用程式</span><span class="sxs-lookup"><span data-stu-id="90c81-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 