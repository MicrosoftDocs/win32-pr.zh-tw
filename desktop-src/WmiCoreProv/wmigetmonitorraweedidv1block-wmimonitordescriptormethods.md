---
description: 取得指定的視頻電子產品標準關聯 () 增強的擴充顯示器識別資料 (E-EDID) 結構的原始資料，以定義設定監視的最佳設定。
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: WmiMonitorDescriptorMethods 類別的 WmiGetMonitorRawEEdidV1Block 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975435"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="95b5d-103">WmiMonitorDescriptorMethods 類別的 WmiGetMonitorRawEEdidV1Block 方法</span><span class="sxs-lookup"><span data-stu-id="95b5d-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="95b5d-104">**WmiGetMonitorRawEEdidV1Block** 方法會取得指定的視頻電子產品標準關聯 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構，以定義監視設定的最佳設定。</span><span class="sxs-lookup"><span data-stu-id="95b5d-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="95b5d-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="95b5d-106">參數</span><span class="sxs-lookup"><span data-stu-id="95b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b5d-107">*區塊識別碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95b5d-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b5d-108">資料區塊識別。</span><span class="sxs-lookup"><span data-stu-id="95b5d-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="95b5d-109">*BlockType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="95b5d-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b5d-110">資料區塊的類型。</span><span class="sxs-lookup"><span data-stu-id="95b5d-110">Type of data block.</span></span> <span data-ttu-id="95b5d-111">下表列出可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="95b5d-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="95b5d-112">值</span><span class="sxs-lookup"><span data-stu-id="95b5d-112">Value</span></span>                                                                                 | <span data-ttu-id="95b5d-113">意義</span><span class="sxs-lookup"><span data-stu-id="95b5d-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="95b5d-114"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="95b5d-115">未初始化：</span><span class="sxs-lookup"><span data-stu-id="95b5d-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="95b5d-116"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="95b5d-117">EDID 基底區塊</span><span class="sxs-lookup"><span data-stu-id="95b5d-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="95b5d-118"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="95b5d-119">EDID 區塊對應</span><span class="sxs-lookup"><span data-stu-id="95b5d-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="95b5d-120"><dt>255 (0xFF) </dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="95b5d-121">其他</span><span class="sxs-lookup"><span data-stu-id="95b5d-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="95b5d-122">*BlockContent* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="95b5d-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b5d-123">128位元組陣列，其中包含原始區塊內容。</span><span class="sxs-lookup"><span data-stu-id="95b5d-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b5d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="95b5d-124">Return value</span></span>

<span data-ttu-id="95b5d-125">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="95b5d-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="95b5d-126">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="95b5d-126">Any other number indicates an error.</span></span> <span data-ttu-id="95b5d-127">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="95b5d-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="95b5d-128">範例</span><span class="sxs-lookup"><span data-stu-id="95b5d-128">Examples</span></span>

<span data-ttu-id="95b5d-129">下列程式碼範例會將任何顯示的 EDID 區塊抓取為原始128位陣列。</span><span class="sxs-lookup"><span data-stu-id="95b5d-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="95b5d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="95b5d-130">Requirements</span></span>



| <span data-ttu-id="95b5d-131">需求</span><span class="sxs-lookup"><span data-stu-id="95b5d-131">Requirement</span></span> | <span data-ttu-id="95b5d-132">值</span><span class="sxs-lookup"><span data-stu-id="95b5d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95b5d-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95b5d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="95b5d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95b5d-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="95b5d-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95b5d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="95b5d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95b5d-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="95b5d-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="95b5d-137">Namespace</span></span><br/>                | <span data-ttu-id="95b5d-138">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="95b5d-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="95b5d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="95b5d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95b5d-140"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="95b5d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="95b5d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b5d-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b5d-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b5d-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95b5d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b5d-144">**WmiMonitorDescriptorMethods**</span><span class="sxs-lookup"><span data-stu-id="95b5d-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="95b5d-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="95b5d-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

