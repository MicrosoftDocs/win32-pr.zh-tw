---
title: objectCategory 與 objectClass
description: ObjectCategory 和 objectClass 屬性都可以參考目錄物件的指定架構類別。
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory 與 objectClass ADSI
- 屬性 ASI、搜尋 objectCategory 和 objectClass 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020795"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="11cf2-105">objectCategory 與 objectClass</span><span class="sxs-lookup"><span data-stu-id="11cf2-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="11cf2-106">**ObjectCategory** 和 **objectClass** 屬性都可以參考目錄物件的指定架構類別。</span><span class="sxs-lookup"><span data-stu-id="11cf2-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="11cf2-107">不過，兩者之間的語義有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="11cf2-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="11cf2-108">「objectClass = 樂趣」指的是這類目錄物件，其中「樂趣」代表物件類別階層中的任何類別。</span><span class="sxs-lookup"><span data-stu-id="11cf2-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="11cf2-109">相反地，"objectCategory = 樂趣" 指的是這些目錄物件，其中「樂趣」會識別物件類別階層中的特定類別。</span><span class="sxs-lookup"><span data-stu-id="11cf2-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="11cf2-110">**objectClass** 可以接受多個值，而 **objectCategory** 會採用單一值。</span><span class="sxs-lookup"><span data-stu-id="11cf2-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="11cf2-111">因此， **objectCategory** 更適合用來比對目錄搜尋中的物件類型。</span><span class="sxs-lookup"><span data-stu-id="11cf2-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="11cf2-112">ADSI 使用這個作為預設比對準則。</span><span class="sxs-lookup"><span data-stu-id="11cf2-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="11cf2-113">使用一個 **objectClass** 的搜尋無法擴充至大型資料庫。</span><span class="sxs-lookup"><span data-stu-id="11cf2-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="11cf2-114">ADSI 支援 " (objectCategory = SomeDN) " 和 " (objectCategory = \_ \_ \_) 類別的 Ldap 顯示名稱 \_ " 語法。</span><span class="sxs-lookup"><span data-stu-id="11cf2-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="11cf2-115">唯一的例外是 LDAP 搜尋篩選「 (objectClass =) 」不 \* 會在物件類別上指定搜尋，而只會測試物件是否存在。</span><span class="sxs-lookup"><span data-stu-id="11cf2-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




