---
title: IConfigAsfWriter GetIndexMode 方法
description: GetIndexMode 方法會抓取目前的時態性索引模式。
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- GetIndexMode 方法 windows Media 格式
- GetIndexMode 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetIndexMode 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375825"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="df2d2-106">IConfigAsfWriter：： GetIndexMode 方法</span><span class="sxs-lookup"><span data-stu-id="df2d2-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="df2d2-107">**GetIndexMode** 方法會抓取目前的時態性索引模式。</span><span class="sxs-lookup"><span data-stu-id="df2d2-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="df2d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="df2d2-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="df2d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="df2d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df2d2-110">*pbIndexFile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df2d2-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df2d2-111">**BOOL** 類型變數的指標，此變數會接收時態性索引模式設定。</span><span class="sxs-lookup"><span data-stu-id="df2d2-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="df2d2-112">**TRUE** 值表示已將 WM ASF 寫入器設定為寫入暫時的索引檔案。</span><span class="sxs-lookup"><span data-stu-id="df2d2-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df2d2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="df2d2-113">Return value</span></span>

<span data-ttu-id="df2d2-114">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="df2d2-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="df2d2-115">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="df2d2-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="df2d2-116">備註</span><span class="sxs-lookup"><span data-stu-id="df2d2-116">Remarks</span></span>

<span data-ttu-id="df2d2-117">使用這個方法來判斷是否目前將 [WM ASF 寫入器](wm-asf-writer-filter.md) 設定為寫入暫時索引的 asf 檔案。</span><span class="sxs-lookup"><span data-stu-id="df2d2-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="df2d2-118">如需暫時索引和框架索引檔案的詳細資訊，請參閱 [**IConfigAsfWriter：： SetIndexMode**](iconfigasfwriter-setindexmode.md)的備註。</span><span class="sxs-lookup"><span data-stu-id="df2d2-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="df2d2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df2d2-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="df2d2-120">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df2d2-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 