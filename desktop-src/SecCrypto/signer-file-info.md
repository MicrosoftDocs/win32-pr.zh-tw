---
description: 指定要簽署的檔案。
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975472"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="471ac-103">簽署者檔案 \_ \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="471ac-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="471ac-104">**簽署者 \_ 檔案 \_ 資訊** 結構會指定要簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="471ac-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="471ac-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="471ac-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="471ac-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="471ac-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="471ac-107">語法</span><span class="sxs-lookup"><span data-stu-id="471ac-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="471ac-108">成員</span><span class="sxs-lookup"><span data-stu-id="471ac-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="471ac-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="471ac-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="471ac-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="471ac-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="471ac-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="471ac-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="471ac-112">以 null 結束的字串指標，其中包含要簽署的檔案名。</span><span class="sxs-lookup"><span data-stu-id="471ac-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="471ac-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="471ac-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="471ac-114">**PwszFileName** 成員所指定檔案的開啟控制碼。</span><span class="sxs-lookup"><span data-stu-id="471ac-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="471ac-115">如果這個成員包含有效的控制碼，則會使用此控制碼來存取檔案。</span><span class="sxs-lookup"><span data-stu-id="471ac-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="471ac-116">這個成員可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="471ac-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="471ac-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="471ac-117">Requirements</span></span>



| <span data-ttu-id="471ac-118">需求</span><span class="sxs-lookup"><span data-stu-id="471ac-118">Requirement</span></span> | <span data-ttu-id="471ac-119">值</span><span class="sxs-lookup"><span data-stu-id="471ac-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="471ac-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="471ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="471ac-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="471ac-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="471ac-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="471ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="471ac-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="471ac-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471ac-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="471ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471ac-125">**簽署者 \_ 主體 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="471ac-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




