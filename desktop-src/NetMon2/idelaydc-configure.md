---
description: Configure 方法會提交用於捕捉的設定資訊。
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: 'IDelaydCConfigure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468744"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="c6481-103">IDelaydC：： Configure 方法</span><span class="sxs-lookup"><span data-stu-id="c6481-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="c6481-104">Configure 方法會提交用於捕捉的 **設定** 資訊。</span><span class="sxs-lookup"><span data-stu-id="c6481-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6481-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6481-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c6481-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6481-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6481-107">*hConfigurationBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6481-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6481-108">包含設定資訊之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6481-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="c6481-109">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6481-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6481-110">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c6481-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="c6481-111">如需錯誤 BLOB 內容的相關資訊，請參閱本主題中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="c6481-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6481-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6481-112">Return value</span></span>

<span data-ttu-id="c6481-113">如果此方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="c6481-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c6481-114">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="c6481-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c6481-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c6481-115">Return code</span></span>                                                                                                      | <span data-ttu-id="c6481-116">Description</span><span class="sxs-lookup"><span data-stu-id="c6481-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6481-117"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="c6481-118">NPP 會報告 capture 會話已啟動。</span><span class="sxs-lookup"><span data-stu-id="c6481-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="c6481-119"><dt>**NMERR \_ 磁片 \_ 未 \_ 固定在本機 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="c6481-120"><dt>**NMERR \_ 無法 \_ \_ 建立 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="c6481-121"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="c6481-122">沒有可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c6481-122">No memory was available.</span></span> <span data-ttu-id="c6481-123">關閉 windows 以釋出資源。</span><span class="sxs-lookup"><span data-stu-id="c6481-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="c6481-124"><dt>**NMERR \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="c6481-125">HConfiguration 參數所指定的設定 BLOB 無效。</span><span class="sxs-lookup"><span data-stu-id="c6481-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6481-126">備註</span><span class="sxs-lookup"><span data-stu-id="c6481-126">Remarks</span></span>

<span data-ttu-id="c6481-127">您必須套用此方法來重新開機已啟動、已停止但未中斷連線的 NPP。</span><span class="sxs-lookup"><span data-stu-id="c6481-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="c6481-128">*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器在 *hConfigurationBlob* 中指定的設定 BLOB 中無法瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="c6481-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="c6481-129">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c6481-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="c6481-130">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="c6481-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6481-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6481-131">Requirements</span></span>



| <span data-ttu-id="c6481-132">需求</span><span class="sxs-lookup"><span data-stu-id="c6481-132">Requirement</span></span> | <span data-ttu-id="c6481-133">值</span><span class="sxs-lookup"><span data-stu-id="c6481-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6481-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6481-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c6481-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6481-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c6481-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6481-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c6481-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6481-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c6481-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c6481-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6481-139"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c6481-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c6481-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6481-141"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6481-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6481-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6481-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6481-143">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="c6481-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c6481-144">IDelaydC：： Connect</span><span class="sxs-lookup"><span data-stu-id="c6481-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c6481-145">IDelaydC：： Start</span><span class="sxs-lookup"><span data-stu-id="c6481-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c6481-146">IDelaydC：： Stop</span><span class="sxs-lookup"><span data-stu-id="c6481-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




