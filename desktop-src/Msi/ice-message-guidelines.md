---
description: ICE 自訂動作會藉由呼叫 MsiProcessMessage 和張貼 INSTALLMESSAGE \_ 使用者類型訊息來進行通訊。
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: ICE 訊息指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943383"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="99eee-103">ICE 訊息指導方針</span><span class="sxs-lookup"><span data-stu-id="99eee-103">ICE Message Guidelines</span></span>

<span data-ttu-id="99eee-104">ICE 自訂動作會藉由呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 和張貼 INSTALLMESSAGE \_ 使用者類型訊息來進行通訊。</span><span class="sxs-lookup"><span data-stu-id="99eee-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="99eee-105">撰寫 ICE 自訂動作的訊息字串時，請將字串格式化，如下所示。</span><span class="sxs-lookup"><span data-stu-id="99eee-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="99eee-106">*ICE* <tab> 的名稱 *訊息類型* <tab>*描述* <tab>說明 *URL 或位置* <tab>*資料表名稱* <tab>資料 *行名稱* <tab>*主要金鑰* <tab>*主要金鑰* <tab>*主鍵*。</span><span class="sxs-lookup"><span data-stu-id="99eee-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="99eee-107">.</span><span class="sxs-lookup"><span data-stu-id="99eee-107">.</span></span> <span data-ttu-id="99eee-108">.</span><span class="sxs-lookup"><span data-stu-id="99eee-108">.</span></span> <span data-ttu-id="99eee-109"> (視需要針對多個主要金鑰重複執行) </span><span class="sxs-lookup"><span data-stu-id="99eee-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="99eee-110">每個訊息中都需要字串的前三個欄位。</span><span class="sxs-lookup"><span data-stu-id="99eee-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="99eee-111">[訊息類型] 欄位會指定 ICE 是否報告失敗、錯誤、警告或告知性訊息。</span><span class="sxs-lookup"><span data-stu-id="99eee-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="99eee-112">值</span><span class="sxs-lookup"><span data-stu-id="99eee-112">Value</span></span> | <span data-ttu-id="99eee-113">訊息類型</span><span class="sxs-lookup"><span data-stu-id="99eee-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99eee-114">0</span><span class="sxs-lookup"><span data-stu-id="99eee-114">0</span></span>     | <span data-ttu-id="99eee-115">報告 ICE 自訂動作失敗的失敗訊息。</span><span class="sxs-lookup"><span data-stu-id="99eee-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="99eee-116">1</span><span class="sxs-lookup"><span data-stu-id="99eee-116">1</span></span>     | <span data-ttu-id="99eee-117">導致不正確行為的錯誤訊息報告資料庫撰寫。</span><span class="sxs-lookup"><span data-stu-id="99eee-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="99eee-118">2</span><span class="sxs-lookup"><span data-stu-id="99eee-118">2</span></span>     | <span data-ttu-id="99eee-119">在某些情況下導致不正確行為的警告訊息報告資料庫撰寫。</span><span class="sxs-lookup"><span data-stu-id="99eee-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="99eee-120">警告也可以報告資料庫撰寫的非預期副作用。</span><span class="sxs-lookup"><span data-stu-id="99eee-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="99eee-121">3</span><span class="sxs-lookup"><span data-stu-id="99eee-121">3</span></span>     | <span data-ttu-id="99eee-122">參考資訊。</span><span class="sxs-lookup"><span data-stu-id="99eee-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="99eee-123">如果無法使用 [說明]，[說明 URL] 欄位可能是空字串。</span><span class="sxs-lookup"><span data-stu-id="99eee-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="99eee-124">錯誤和警告訊息應該提供資料表名稱、資料行名稱和主要索引鍵欄位。</span><span class="sxs-lookup"><span data-stu-id="99eee-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="99eee-125">如果省略這些欄位中的任何欄位，則在第一個空白欄位之後的所有欄位都必須留出訊息。</span><span class="sxs-lookup"><span data-stu-id="99eee-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="99eee-126">例如，提供的資料表名稱沒有資料行名稱和主鍵或資料表名稱，而且沒有主鍵的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="99eee-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="99eee-127">不過，資料行名稱和主鍵不能在沒有資料表名稱的情況下使用。</span><span class="sxs-lookup"><span data-stu-id="99eee-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="99eee-128">在該資料表中的所有主鍵都已指定值之前，可能會列出多個主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="99eee-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="99eee-129">範例</span><span class="sxs-lookup"><span data-stu-id="99eee-129">Examples</span></span>

<span data-ttu-id="99eee-130">[C + + 中範例 ICE](sample-ice-in-c-.md)所說明的第一則訊息：</span><span class="sxs-lookup"><span data-stu-id="99eee-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="99eee-131">"ICE01 \\ t3 \\ t 已建立 04/29/1998 by <在此處插入作者名稱>。</span><span class="sxs-lookup"><span data-stu-id="99eee-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="99eee-132">範例 ICE 所公佈的第二個訊息：</span><span class="sxs-lookup"><span data-stu-id="99eee-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="99eee-133">「ICE01 \\ t3 \\ tLast 修改了05/06/1999，<在此處插入作者的名稱>。」</span><span class="sxs-lookup"><span data-stu-id="99eee-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="99eee-134">範例 ICE 所公佈的第三個訊息。</span><span class="sxs-lookup"><span data-stu-id="99eee-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="99eee-135">「ICE01 \\ t3 \\ tSimple 冰以說明霜淇淋概念」。</span><span class="sxs-lookup"><span data-stu-id="99eee-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



