---
description: 設定與 DDE 共用相關聯的安全描述項。
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: 'NDdeSetShareSecurity 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987255"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="f5bb0-103">NDdeSetShareSecurity 函式</span><span class="sxs-lookup"><span data-stu-id="f5bb0-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="f5bb0-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="f5bb0-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="f5bb0-106">設定與 DDE 共用相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="f5bb0-107">這通常是在編輯指派給 DDE 共用的 DACL 之後完成。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bb0-108">語法</span><span class="sxs-lookup"><span data-stu-id="f5bb0-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="f5bb0-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5bb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bb0-110">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bb0-111">要修改其 DSDM 的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb0-112">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bb0-113">要修改其安全描述項的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="f5bb0-114">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb0-115">*si* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bb0-116">[**安全性 \_ 資訊**](/windows/desktop/SecAuthZ/security-information)值，可識別要取出的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb0-117">*pSD* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bb0-118">[**安全性 \_ 描述**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)元結構的指標，其中包含安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="f5bb0-119">此參數不可以是 **Null** ，而且應指向有效的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5bb0-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5bb0-120">Return value</span></span>

<span data-ttu-id="f5bb0-121">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="f5bb0-122">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5bb0-123">備註</span><span class="sxs-lookup"><span data-stu-id="f5bb0-123">Remarks</span></span>

<span data-ttu-id="f5bb0-124">若要修改與 DSDM 中的 DDE 共用相關聯的 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) ，使用者必須具有適當的許可權; 共用建立者具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="f5bb0-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bb0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5bb0-125">Requirements</span></span>



| <span data-ttu-id="f5bb0-126">需求</span><span class="sxs-lookup"><span data-stu-id="f5bb0-126">Requirement</span></span> | <span data-ttu-id="f5bb0-127">值</span><span class="sxs-lookup"><span data-stu-id="f5bb0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bb0-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5bb0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bb0-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5bb0-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5bb0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bb0-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5bb0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f5bb0-132">標頭</span><span class="sxs-lookup"><span data-stu-id="f5bb0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5bb0-133"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5bb0-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5bb0-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5bb0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5bb0-135"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5bb0-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5bb0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f5bb0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5bb0-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5bb0-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5bb0-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f5bb0-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f5bb0-139">**NDdeSetShareSecurityW** (Unicode) 和 **NDdeSetShareSecurityA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f5bb0-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="f5bb0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5bb0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bb0-141">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="f5bb0-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="f5bb0-142">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="f5bb0-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="f5bb0-143">**安全性 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f5bb0-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="f5bb0-144">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="f5bb0-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

