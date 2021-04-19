---
description: 建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: 'NDdeShareAdd 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984675"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="b8e01-103">NDdeShareAdd 函式</span><span class="sxs-lookup"><span data-stu-id="b8e01-103">NDdeShareAdd function</span></span>

<span data-ttu-id="b8e01-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="b8e01-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b8e01-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b8e01-106">建立新的 DDE 共用，並將其新增至 DDE 共用資料庫管理員 (DSDM) 。</span><span class="sxs-lookup"><span data-stu-id="b8e01-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e01-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8e01-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="b8e01-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e01-109">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-110">要修改其 DSDM 的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8e01-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-111">*nLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-112">資訊層級。</span><span class="sxs-lookup"><span data-stu-id="b8e01-112">The information level.</span></span> <span data-ttu-id="b8e01-113">此參數必須是2。</span><span class="sxs-lookup"><span data-stu-id="b8e01-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-114">*pSD* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-115">要與此共用相關聯之 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構的指標，以及將在後續起始至此共用時執行的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="b8e01-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="b8e01-116">這個參數可以是 **Null**，在此情況下，DSDM 會建立預設安全描述項，將「完全控制」授與擁有者，並將「讀取和連結」授與所有人。</span><span class="sxs-lookup"><span data-stu-id="b8e01-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-117">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-118">[**NDDESHAREINFO**](nddeshareinfo-str.md)結構的指標，此結構會定義與所建立之 DDE 共用相關聯的 ApplicationTopic 清單以及其他參數。</span><span class="sxs-lookup"><span data-stu-id="b8e01-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="b8e01-119">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8e01-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-120">*cBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-121">*LpBuffer* 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8e01-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="b8e01-122">此參數不可以是零。</span><span class="sxs-lookup"><span data-stu-id="b8e01-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e01-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8e01-123">Return value</span></span>

<span data-ttu-id="b8e01-124">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="b8e01-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="b8e01-125">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b8e01-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e01-126">備註</span><span class="sxs-lookup"><span data-stu-id="b8e01-126">Remarks</span></span>

<span data-ttu-id="b8e01-127">在用戶端可以連線到 DDE 共用之前，必須先使用 [**NDdeSetTrustedShare**](nddesettrustedshare.md)來信任它。</span><span class="sxs-lookup"><span data-stu-id="b8e01-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e01-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8e01-128">Requirements</span></span>



| <span data-ttu-id="b8e01-129">需求</span><span class="sxs-lookup"><span data-stu-id="b8e01-129">Requirement</span></span> | <span data-ttu-id="b8e01-130">值</span><span class="sxs-lookup"><span data-stu-id="b8e01-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e01-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8e01-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e01-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8e01-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8e01-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e01-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8e01-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b8e01-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8e01-136"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e01-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8e01-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8e01-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8e01-138"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8e01-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8e01-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e01-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8e01-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e01-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8e01-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b8e01-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8e01-142">**NDdeShareAddW** (Unicode) 和 **NDdeShareAddA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b8e01-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="b8e01-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e01-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e01-144">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="b8e01-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b8e01-145">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="b8e01-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="b8e01-146">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="b8e01-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="b8e01-147">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="b8e01-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

