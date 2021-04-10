---
description: 磁片區陰影複製 API 中定義了下列資料類型：
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: 磁片區陰影複製 API 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690468"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="b0ae4-103">磁片區陰影複製 API 資料類型</span><span class="sxs-lookup"><span data-stu-id="b0ae4-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="b0ae4-104">磁片區陰影複製 API 中定義了下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="b0ae4-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="b0ae4-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b0ae4-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="b0ae4-106">**Vss 識別碼 \_** 定義會指定一般 VSS 識別碼格式。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="b0ae4-107">**VSS \_ 識別碼** 是標準的 GUID 資料類型。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="b0ae4-108">**VSS \_識別碼** 是用來識別下列各項：陰影複製、陰影複製集、提供者、提供者版本、寫入器 (寫入器的類別識別碼) 和寫入器的實例。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="b0ae4-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ</span><span class="sxs-lookup"><span data-stu-id="b0ae4-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="b0ae4-110">**VSS \_ PWSZ** 定義會指定以 null 終止的寬字元字串， (wchar) 。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="b0ae4-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="b0ae4-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="b0ae4-112">**VSS \_ 時間戳記** 定義會將時間戳記資訊保存為64位整數值，其中包含自年1月1日起 1601 (UTC) 的100秒數間隔。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="b0ae4-113">這項定義可與 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構互換。</span><span class="sxs-lookup"><span data-stu-id="b0ae4-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
