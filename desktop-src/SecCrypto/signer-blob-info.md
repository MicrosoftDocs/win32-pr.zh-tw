---
description: 指定要簽署的 BLOB。
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514188"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="85765-103">簽署者 \_ BLOB \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="85765-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="85765-104">\[您可以在 [需求] 區段中指定的作業系統中使用 **簽署者 \_ BLOB \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="85765-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="85765-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="85765-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="85765-106">**簽署者 \_ BLOB \_ 資訊** 結構會指定要簽署的 [*blob*](../secgloss/b-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="85765-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="85765-107">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="85765-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="85765-108">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="85765-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85765-109">語法</span><span class="sxs-lookup"><span data-stu-id="85765-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="85765-110">成員</span><span class="sxs-lookup"><span data-stu-id="85765-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="85765-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="85765-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="85765-112">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="85765-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="85765-113">**pGuidSubject**</span><span class="sxs-lookup"><span data-stu-id="85765-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="85765-114">**GUID** 的指標，指定要載入 (SIP) 的主體介面套件。</span><span class="sxs-lookup"><span data-stu-id="85765-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="85765-115">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="85765-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="85765-116">要簽署之 BLOB 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="85765-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="85765-117">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="85765-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="85765-118">要簽署之 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="85765-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="85765-119">**pwszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="85765-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="85765-120">BLOB 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="85765-120">The display name of the BLOB.</span></span> <span data-ttu-id="85765-121">這個成員可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85765-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85765-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="85765-122">Requirements</span></span>



| <span data-ttu-id="85765-123">需求</span><span class="sxs-lookup"><span data-stu-id="85765-123">Requirement</span></span> | <span data-ttu-id="85765-124">值</span><span class="sxs-lookup"><span data-stu-id="85765-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85765-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85765-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85765-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85765-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="85765-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85765-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85765-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85765-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85765-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85765-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85765-130">**簽署者 \_ 主體 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="85765-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
