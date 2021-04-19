---
description: 安裝程式會提供可操作安裝資料庫中記錄的函式。 這些函數可與使用查詢中所述的函式搭配使用，以在資料庫中進行實際變更。
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: 使用記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980343"
---
# <a name="working-with-records"></a><span data-ttu-id="deba0-104">使用記錄</span><span class="sxs-lookup"><span data-stu-id="deba0-104">Working with Records</span></span>

<span data-ttu-id="deba0-105">安裝程式會提供可操作安裝資料庫中記錄的函式。</span><span class="sxs-lookup"><span data-stu-id="deba0-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="deba0-106">這些函數可與 [使用查詢](working-with-queries.md) 中所述的函式搭配使用，以在資料庫中進行實際變更。</span><span class="sxs-lookup"><span data-stu-id="deba0-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="deba0-107">下列函數會建立或移除記錄：</span><span class="sxs-lookup"><span data-stu-id="deba0-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="deba0-108">若要建立資料庫的新記錄，請呼叫 [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="deba0-109">若要清除記錄中的資料，請呼叫 [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) 函數，將每個欄位設定為 null。</span><span class="sxs-lookup"><span data-stu-id="deba0-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="deba0-110">下列函數會填滿指定的記錄欄位：</span><span class="sxs-lookup"><span data-stu-id="deba0-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="deba0-111">若要將記錄設定為整數，請呼叫 [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="deba0-112">若要將記錄設定為字串，請呼叫 [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="deba0-113">若要將整個檔案插入資料流程欄位中，請呼叫 [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="deba0-114">下列函數會從指定的記錄欄位讀取值：</span><span class="sxs-lookup"><span data-stu-id="deba0-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="deba0-115">若要從欄位讀取整數值，請呼叫 [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="deba0-116">若要取出字串值，請呼叫 [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="deba0-117">若要取得資料流程，請呼叫 [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="deba0-118">若要判斷記錄的特定欄位是否為 null，請呼叫 [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="deba0-119">下列函式是資訊記錄函數：</span><span class="sxs-lookup"><span data-stu-id="deba0-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="deba0-120">若要取得記錄包含的欄位數目，請呼叫 [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="deba0-121">若要取得欄位的大小，請呼叫 [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) 函數。</span><span class="sxs-lookup"><span data-stu-id="deba0-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="deba0-122">**MsiRecordDataSize** 的傳回值是對欄位類型的敏感性。</span><span class="sxs-lookup"><span data-stu-id="deba0-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



