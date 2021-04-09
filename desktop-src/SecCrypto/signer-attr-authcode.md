---
description: 指定 Authenticode 簽章的屬性。
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945394"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="9d04e-103">簽署者 \_ ATTR \_ AUTHCODE 結構</span><span class="sxs-lookup"><span data-stu-id="9d04e-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="9d04e-104">**簽署者的 \_ ATTR \_ AUTHCODE** 結構會指定 [*Authenticode*](../secgloss/a-gly.md)簽章的屬性。</span><span class="sxs-lookup"><span data-stu-id="9d04e-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="9d04e-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="9d04e-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="9d04e-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="9d04e-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9d04e-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d04e-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="9d04e-108">成員</span><span class="sxs-lookup"><span data-stu-id="9d04e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d04e-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="9d04e-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="9d04e-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9d04e-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d04e-111">**fCommercial**</span><span class="sxs-lookup"><span data-stu-id="9d04e-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="9d04e-112">**TRUE** 表示將主體簽署為商業發行者;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9d04e-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9d04e-113">**fIndividual**</span><span class="sxs-lookup"><span data-stu-id="9d04e-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="9d04e-114">**TRUE** 表示以個別發行者的形式簽署主體;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9d04e-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9d04e-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="9d04e-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="9d04e-116">下載時檔案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9d04e-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="9d04e-117">**pwszInfo**</span><span class="sxs-lookup"><span data-stu-id="9d04e-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="9d04e-118">下載時檔案的 URL 顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9d04e-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d04e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d04e-119">Requirements</span></span>



| <span data-ttu-id="9d04e-120">需求</span><span class="sxs-lookup"><span data-stu-id="9d04e-120">Requirement</span></span> | <span data-ttu-id="9d04e-121">值</span><span class="sxs-lookup"><span data-stu-id="9d04e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d04e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d04e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9d04e-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d04e-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9d04e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d04e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9d04e-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d04e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d04e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d04e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d04e-127">**簽署人 \_ 簽名 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9d04e-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
