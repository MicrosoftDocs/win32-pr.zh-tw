---
description: KEYSVC \_ unicode \_ 字串結構會定義 unicode 字串和字串的最大長度。 RKeyPFXInstall 函數會使用這個結構。
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: 'KEYSVC_UNICODE_STRING 結構 (Rkeysvcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975337"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="6787d-104">KEYSVC \_ UNICODE \_ 字串結構</span><span class="sxs-lookup"><span data-stu-id="6787d-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="6787d-105">**KEYSVC \_ unicode \_ 字串** 結構會定義 [*unicode*](../secgloss/u-gly.md)字串和字串的最大長度。</span><span class="sxs-lookup"><span data-stu-id="6787d-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="6787d-106">[**RKeyPFXInstall**](rkeypfxinstall.md)函數會使用這個結構。</span><span class="sxs-lookup"><span data-stu-id="6787d-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6787d-107">語法</span><span class="sxs-lookup"><span data-stu-id="6787d-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="6787d-108">成員</span><span class="sxs-lookup"><span data-stu-id="6787d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6787d-109">**長度**</span><span class="sxs-lookup"><span data-stu-id="6787d-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="6787d-110">**USHORT** 值，指定用於 **緩衝區** 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6787d-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="6787d-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="6787d-112">**USHORT** 值，指定 **緩衝區** 允許的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6787d-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="6787d-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="6787d-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="6787d-114">表示 Unicode 字串的 **USHORT** 指標。</span><span class="sxs-lookup"><span data-stu-id="6787d-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6787d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6787d-115">Requirements</span></span>



| <span data-ttu-id="6787d-116">需求</span><span class="sxs-lookup"><span data-stu-id="6787d-116">Requirement</span></span> | <span data-ttu-id="6787d-117">值</span><span class="sxs-lookup"><span data-stu-id="6787d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6787d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6787d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6787d-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6787d-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6787d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6787d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6787d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6787d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6787d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6787d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6787d-123"><dt>Rkeysvcc。h</dt></span><span class="sxs-lookup"><span data-stu-id="6787d-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6787d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6787d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6787d-125">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="6787d-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="6787d-126">**KEYSVC \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="6787d-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
