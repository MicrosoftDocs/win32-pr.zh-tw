---
description: 在目前的使用者內容中，授與指定的 DDE 共用信任狀態。
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: 'NDdeSetTrustedShare 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510913"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="8d9ed-103">NDdeSetTrustedShare 函式</span><span class="sxs-lookup"><span data-stu-id="8d9ed-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="8d9ed-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="8d9ed-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="8d9ed-106">在目前使用者的內容中，授與指定的 DDE 共用信任狀態。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d9ed-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="8d9ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d9ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9ed-109">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-110">要修改其 DSDM 的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ed-111">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-112">要授與受信任狀態的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="8d9ed-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ed-114">*dwTrustOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-115">影響 DDE 共用之受信任狀態的選項。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="8d9ed-116">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8d9ed-117">選項</span><span class="sxs-lookup"><span data-stu-id="8d9ed-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8d9ed-118">意義</span><span class="sxs-lookup"><span data-stu-id="8d9ed-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="8d9ed-119"><dt>**NDDE \_CMD \_ 顯示 \_ 遮罩**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="8d9ed-120">如果 \_ \_ 已設定 NDDE TRUST CMD show，則用來取得用來覆寫「DDE 共用顯示」狀態之值的遮罩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="8d9ed-121"><dt>**NDDE \_信任 \_ CMD \_ 顯示**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="8d9ed-122">覆寫 [DDE 共用 DSDM] 中指定的顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="8d9ed-123"><dt>**NDDE \_信任 \_ 共用 \_ DEL**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="8d9ed-124">移除共用的受信任狀態。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="8d9ed-125"><dt>**NDDE \_信任 \_ 共用 \_ INIT**</dt> <dt>0x40000000L</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="8d9ed-126">如果應用程式已在使用者的內容中執行，則允許用戶端起始該應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="8d9ed-127"><dt>**NDDE \_信任 \_ 共用 \_ 開始**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="8d9ed-128">允許在使用者的內容中啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9ed-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d9ed-129">Return value</span></span>

<span data-ttu-id="8d9ed-130">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="8d9ed-131">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9ed-132">備註</span><span class="sxs-lookup"><span data-stu-id="8d9ed-132">Remarks</span></span>

<span data-ttu-id="8d9ed-133">必須先使用 [**NDdeShareAdd**](nddeshareadd.md)建立 DDE 共用。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="8d9ed-134">如果呼叫 **NDdeSetTrustedShare** 時， *dwTrustOptions* 設定為零，則受信任的共用會失去其受信任的狀態。</span><span class="sxs-lookup"><span data-stu-id="8d9ed-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d9ed-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d9ed-135">Requirements</span></span>



| <span data-ttu-id="8d9ed-136">需求</span><span class="sxs-lookup"><span data-stu-id="8d9ed-136">Requirement</span></span> | <span data-ttu-id="8d9ed-137">值</span><span class="sxs-lookup"><span data-stu-id="8d9ed-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9ed-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d9ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9ed-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d9ed-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d9ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9ed-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d9ed-142">標頭</span><span class="sxs-lookup"><span data-stu-id="8d9ed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d9ed-143"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d9ed-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d9ed-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d9ed-145"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d9ed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8d9ed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d9ed-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d9ed-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8d9ed-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8d9ed-149">**NDdeSetTrustedShareW** (Unicode) 和 **NDdeSetTrustedShareA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8d9ed-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="8d9ed-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d9ed-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9ed-151">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="8d9ed-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="8d9ed-152">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="8d9ed-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="8d9ed-153">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




