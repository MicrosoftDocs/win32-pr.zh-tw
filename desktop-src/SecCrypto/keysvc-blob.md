---
description: KEYSVC \_ BLOB 結構會定義金鑰服務 blob。 RKeyPFXInstall 函數會使用這個結構。
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: 'KEYSVC_BLOB 結構 (Rkeysvcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992184"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="501ca-104">KEYSVC \_ BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="501ca-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="501ca-105">**KEYSVC \_ BLOB** 結構會定義金鑰服務 blob。</span><span class="sxs-lookup"><span data-stu-id="501ca-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="501ca-106">[**RKeyPFXInstall**](rkeypfxinstall.md)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="501ca-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="501ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="501ca-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="501ca-108">成員</span><span class="sxs-lookup"><span data-stu-id="501ca-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="501ca-109">**Cb**</span><span class="sxs-lookup"><span data-stu-id="501ca-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="501ca-110">指定大小（以位元組為單位）的 **ULONG** 值（以 **位元組為單位）。**</span><span class="sxs-lookup"><span data-stu-id="501ca-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="501ca-111">**鉛**</span><span class="sxs-lookup"><span data-stu-id="501ca-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="501ca-112">包含 BLOB 的 **位元組** 指標，採用 [*PKCS \# 12*](../secgloss/p-gly.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="501ca-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="501ca-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="501ca-113">Requirements</span></span>



| <span data-ttu-id="501ca-114">需求</span><span class="sxs-lookup"><span data-stu-id="501ca-114">Requirement</span></span> | <span data-ttu-id="501ca-115">值</span><span class="sxs-lookup"><span data-stu-id="501ca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="501ca-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="501ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="501ca-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="501ca-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="501ca-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="501ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="501ca-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="501ca-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="501ca-120">標頭</span><span class="sxs-lookup"><span data-stu-id="501ca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="501ca-121"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="501ca-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="501ca-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="501ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501ca-123">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="501ca-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="501ca-124">**KEYSVC \_ UNICODE \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="501ca-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
