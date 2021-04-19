---
title: 'WINBIO_EVENT 結構 (Winbio \_ 類型 .h) '
description: 包含引發事件通知時，傳送至回呼常式的狀態資訊。
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EVENT 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968196"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="445f3-105">WINBIO \_ 事件結構</span><span class="sxs-lookup"><span data-stu-id="445f3-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="445f3-106">**WINBIO \_ 事件** 結構包含引發事件通知時，傳送至回呼常式的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="445f3-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="445f3-107">語法</span><span class="sxs-lookup"><span data-stu-id="445f3-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="445f3-108">成員</span><span class="sxs-lookup"><span data-stu-id="445f3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="445f3-109">**型別**</span><span class="sxs-lookup"><span data-stu-id="445f3-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-110">值，指定所引發之服務提供者事件通知的類型。</span><span class="sxs-lookup"><span data-stu-id="445f3-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="445f3-111">目前唯一支援的提供者是指紋感應器。</span><span class="sxs-lookup"><span data-stu-id="445f3-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="445f3-112">此感應器支援下列旗標。</span><span class="sxs-lookup"><span data-stu-id="445f3-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="445f3-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_事件 \_ FP \_ 取消認領** (感應器偵測到應用程式未要求的手指刷，或目前有焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="445f3-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="445f3-114">Windows 生物特徵辨識架構呼叫您的回呼函式，以表示已發生手指刷，但不會嘗試識別指紋。 ) </span><span class="sxs-lookup"><span data-stu-id="445f3-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="445f3-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_事件 \_ FP \_ 取消認領 \_ 識別** (感應器偵測到應用程式未要求的手指刷，或目前有焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="445f3-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="445f3-116">Windows 生物特徵辨識架構會嘗試識別指紋，並將該進程的結果傳遞給回呼函式。 ) </span><span class="sxs-lookup"><span data-stu-id="445f3-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="445f3-117">**參數**</span><span class="sxs-lookup"><span data-stu-id="445f3-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="445f3-118">**無人 認領**</span><span class="sxs-lookup"><span data-stu-id="445f3-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-119">針對生物特徵辨識範例抓取傳回的結構。</span><span class="sxs-lookup"><span data-stu-id="445f3-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="445f3-120">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="445f3-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-121">產生範例的生物特徵辨識單位。</span><span class="sxs-lookup"><span data-stu-id="445f3-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="445f3-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="445f3-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-123">**ULONG** 值，包含無法捕捉生物特徵辨識範例的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="445f3-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="445f3-124">如果捕捉成功，這個參數會設定為零。</span><span class="sxs-lookup"><span data-stu-id="445f3-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="445f3-125">下列是針對指紋捕捉定義的值：</span><span class="sxs-lookup"><span data-stu-id="445f3-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="445f3-126">WINBIO \_ FP \_ 太 \_ 高</span><span class="sxs-lookup"><span data-stu-id="445f3-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="445f3-127">WINBIO \_ FP \_ 太 \_ 低</span><span class="sxs-lookup"><span data-stu-id="445f3-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="445f3-128">WINBIO \_ FP \_ 太 \_ 左邊</span><span class="sxs-lookup"><span data-stu-id="445f3-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="445f3-129">WINBIO \_ FP \_ 太 \_ 右邊</span><span class="sxs-lookup"><span data-stu-id="445f3-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="445f3-130">WINBIO \_ FP \_ 太 \_ 快</span><span class="sxs-lookup"><span data-stu-id="445f3-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="445f3-131">WINBIO \_ FP \_ 太 \_ 慢</span><span class="sxs-lookup"><span data-stu-id="445f3-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="445f3-132">WINBIO \_ FP \_ 品質不佳 \_</span><span class="sxs-lookup"><span data-stu-id="445f3-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="445f3-133">WINBIO \_ FP \_ 太 \_ 扭曲</span><span class="sxs-lookup"><span data-stu-id="445f3-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="445f3-134">WINBIO \_ FP \_ 太 \_ 短</span><span class="sxs-lookup"><span data-stu-id="445f3-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="445f3-135">WINBIO \_ FP \_ 合併 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="445f3-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="445f3-136">**UnclaimedIdentify**</span><span class="sxs-lookup"><span data-stu-id="445f3-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-137">針對生物特徵辨識捕捉和識別傳回的結構。</span><span class="sxs-lookup"><span data-stu-id="445f3-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="445f3-138">識別可判斷範例是否可以與現有的生物特徵辨識範本相關聯。</span><span class="sxs-lookup"><span data-stu-id="445f3-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="445f3-139">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="445f3-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-140">產生範例的生物特徵辨識單位。</span><span class="sxs-lookup"><span data-stu-id="445f3-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="445f3-141">**身分識別**</span><span class="sxs-lookup"><span data-stu-id="445f3-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-142">[**WINBIO \_ 識別**](winbio-identity.md)結構，其中包含提供生物特徵辨識範例之使用者的 GUID 或 SID。</span><span class="sxs-lookup"><span data-stu-id="445f3-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="445f3-143">**SubFactor**</span><span class="sxs-lookup"><span data-stu-id="445f3-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-144">[**WINBIO \_ 生物特徵辨識 \_ 子類型**](winbio-biometric-subtype-constants.md)值，指定與生物特徵辨識範例相關聯的輔助因素。</span><span class="sxs-lookup"><span data-stu-id="445f3-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="445f3-145">Windows 生物特徵辨識架構 (WBF) 目前僅支援指紋捕捉，並使用下列常數來表示子類型資訊。</span><span class="sxs-lookup"><span data-stu-id="445f3-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="445f3-146">WINBIO \_ ANSI \_ 381 \_ POS \_ 不明</span><span class="sxs-lookup"><span data-stu-id="445f3-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="445f3-147">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB</span><span class="sxs-lookup"><span data-stu-id="445f3-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="445f3-148">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 食指 \_</span><span class="sxs-lookup"><span data-stu-id="445f3-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="445f3-149">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="445f3-150">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="445f3-151">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="445f3-152">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 經驗</span><span class="sxs-lookup"><span data-stu-id="445f3-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="445f3-153">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 索引 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="445f3-154">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="445f3-155">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="445f3-156">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="445f3-157">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="445f3-158">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="445f3-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="445f3-159">WINBIO \_ ANSI \_ 381 \_ POS \_ 雙 \_ 拇指</span><span class="sxs-lookup"><span data-stu-id="445f3-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="445f3-160">請勿嘗試驗證針對 *SubFactor* 值提供的值。</span><span class="sxs-lookup"><span data-stu-id="445f3-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="445f3-161">Windows 生物識別服務會先驗證提供的值，再將其傳遞至您的實作為。</span><span class="sxs-lookup"><span data-stu-id="445f3-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="445f3-162">如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。</span><span class="sxs-lookup"><span data-stu-id="445f3-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="445f3-163">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="445f3-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-164">**ULONG** 值，包含無法捕捉生物特徵辨識範例的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="445f3-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="445f3-165">如果捕捉成功，這個參數會設定為零。</span><span class="sxs-lookup"><span data-stu-id="445f3-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="445f3-166">下列是針對指紋捕捉定義的值：</span><span class="sxs-lookup"><span data-stu-id="445f3-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="445f3-167">WINBIO \_ FP \_ 太 \_ 高</span><span class="sxs-lookup"><span data-stu-id="445f3-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="445f3-168">WINBIO \_ FP \_ 太 \_ 低</span><span class="sxs-lookup"><span data-stu-id="445f3-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="445f3-169">WINBIO \_ FP \_ 太 \_ 左邊</span><span class="sxs-lookup"><span data-stu-id="445f3-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="445f3-170">WINBIO \_ FP \_ 太 \_ 右邊</span><span class="sxs-lookup"><span data-stu-id="445f3-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="445f3-171">WINBIO \_ FP \_ 太 \_ 快</span><span class="sxs-lookup"><span data-stu-id="445f3-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="445f3-172">WINBIO \_ FP \_ 太 \_ 慢</span><span class="sxs-lookup"><span data-stu-id="445f3-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="445f3-173">WINBIO \_ FP \_ 品質不佳 \_</span><span class="sxs-lookup"><span data-stu-id="445f3-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="445f3-174">WINBIO \_ FP \_ 太 \_ 扭曲</span><span class="sxs-lookup"><span data-stu-id="445f3-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="445f3-175">WINBIO \_ FP \_ 太 \_ 短</span><span class="sxs-lookup"><span data-stu-id="445f3-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="445f3-176">WINBIO \_ FP \_ 合併 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="445f3-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="445f3-177">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="445f3-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-178">識別要監視之作業成功或失敗的結構。</span><span class="sxs-lookup"><span data-stu-id="445f3-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="445f3-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="445f3-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="445f3-180">**HRESULT** 值，包含 \_ 由 Windows 生物特徵辨識架構所執行的計算所產生的 [確定] 或 [錯誤碼]。</span><span class="sxs-lookup"><span data-stu-id="445f3-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="445f3-181">備註</span><span class="sxs-lookup"><span data-stu-id="445f3-181">Remarks</span></span>

<span data-ttu-id="445f3-182">呼叫 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) 函式以註冊回呼常式，以從 Windows 生物特徵辨識架構接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="445f3-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="445f3-183">回呼是您必須為應用程式定義的自訂函數。</span><span class="sxs-lookup"><span data-stu-id="445f3-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="445f3-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="445f3-184">Requirements</span></span>



| <span data-ttu-id="445f3-185">需求</span><span class="sxs-lookup"><span data-stu-id="445f3-185">Requirement</span></span> | <span data-ttu-id="445f3-186">值</span><span class="sxs-lookup"><span data-stu-id="445f3-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="445f3-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="445f3-187">Minimum supported client</span></span><br/> | <span data-ttu-id="445f3-188">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445f3-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="445f3-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="445f3-189">Minimum supported server</span></span><br/> | <span data-ttu-id="445f3-190">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="445f3-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="445f3-191">標頭</span><span class="sxs-lookup"><span data-stu-id="445f3-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="445f3-192"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="445f3-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445f3-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="445f3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445f3-194">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="445f3-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="445f3-195">**WinBioRegisterEventMonitor**</span><span class="sxs-lookup"><span data-stu-id="445f3-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





