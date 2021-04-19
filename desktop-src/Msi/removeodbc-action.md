---
description: RemoveODBC 動作會移除在安裝期間列出要移除的資料來源、轉譯程式和驅動程式。
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: RemoveODBC 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988803"
---
# <a name="removeodbc-action"></a><span data-ttu-id="fddb4-103">RemoveODBC 動作</span><span class="sxs-lookup"><span data-stu-id="fddb4-103">RemoveODBC Action</span></span>

<span data-ttu-id="fddb4-104">RemoveODBC 動作會移除在安裝期間列出要移除的資料來源、轉譯程式和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fddb4-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="fddb4-105">此動作會查詢已排程要移除的每個資料來源、翻譯工具或驅動程式的 [ODBCDataSource 資料表](odbcdatasource-table.md)、 [ODBCTranslator 資料表](odbctranslator-table.md)和 [ODBCDriver 資料表](odbcdriver-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="fddb4-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fddb4-106">順序限制</span><span class="sxs-lookup"><span data-stu-id="fddb4-106">Sequence Restrictions</span></span>

<span data-ttu-id="fddb4-107">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="fddb4-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fddb4-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="fddb4-108">ActionData Messages</span></span>

<span data-ttu-id="fddb4-109">每個安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="fddb4-109">For each driver installed.</span></span>



| <span data-ttu-id="fddb4-110">欄位</span><span class="sxs-lookup"><span data-stu-id="fddb4-110">Field</span></span> | <span data-ttu-id="fddb4-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="fddb4-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="fddb4-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-112">\[1\]</span></span> | <span data-ttu-id="fddb4-113">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="fddb4-113">Driver description.</span></span> <span data-ttu-id="fddb4-114">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="fddb4-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="fddb4-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-115">\[2\]</span></span> | <span data-ttu-id="fddb4-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="fddb4-116">ComponentId</span></span>                              |



 

<span data-ttu-id="fddb4-117">針對每個已安裝的翻譯工具。</span><span class="sxs-lookup"><span data-stu-id="fddb4-117">For each translator installed.</span></span>



| <span data-ttu-id="fddb4-118">欄位</span><span class="sxs-lookup"><span data-stu-id="fddb4-118">Field</span></span> | <span data-ttu-id="fddb4-119">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="fddb4-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="fddb4-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-120">\[1\]</span></span> | <span data-ttu-id="fddb4-121">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="fddb4-121">Driver description.</span></span> <span data-ttu-id="fddb4-122">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="fddb4-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="fddb4-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-123">\[2\]</span></span> | <span data-ttu-id="fddb4-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="fddb4-124">ComponentId</span></span>                              |



 

<span data-ttu-id="fddb4-125">針對每個已安裝的資料來源。</span><span class="sxs-lookup"><span data-stu-id="fddb4-125">For each data source installed.</span></span>



| <span data-ttu-id="fddb4-126">欄位</span><span class="sxs-lookup"><span data-stu-id="fddb4-126">Field</span></span> | <span data-ttu-id="fddb4-127">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="fddb4-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="fddb4-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-128">\[1\]</span></span> | <span data-ttu-id="fddb4-129">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="fddb4-129">Driver description.</span></span> <span data-ttu-id="fddb4-130">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="fddb4-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="fddb4-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-131">\[2\]</span></span> | <span data-ttu-id="fddb4-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="fddb4-132">ComponentId</span></span>                                             |
| <span data-ttu-id="fddb4-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="fddb4-133">\[3\]</span></span> | <span data-ttu-id="fddb4-134">註冊： SQL \_ 移除 \_ DSN 或 sql \_ 移除 \_ SYS \_ DSN</span><span class="sxs-lookup"><span data-stu-id="fddb4-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fddb4-135">備註</span><span class="sxs-lookup"><span data-stu-id="fddb4-135">Remarks</span></span>

<span data-ttu-id="fddb4-136">如果 ODBC 使用計數和檔案使用計數都變成零，則會移除該檔案。</span><span class="sxs-lookup"><span data-stu-id="fddb4-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="fddb4-137">註冊相依于 ODBC 使用計數，而檔案移除是以共用 Dll 金鑰參考計數為基礎。</span><span class="sxs-lookup"><span data-stu-id="fddb4-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



