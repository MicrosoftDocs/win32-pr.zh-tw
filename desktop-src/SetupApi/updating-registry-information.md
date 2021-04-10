---
description: 成功認可佇列之後，您將需要更新您要安裝之產品的登錄資訊。
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: 更新登錄資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944937"
---
# <a name="updating-registry-information"></a><span data-ttu-id="c242a-103">更新登錄資訊</span><span class="sxs-lookup"><span data-stu-id="c242a-103">Updating Registry Information</span></span>

<span data-ttu-id="c242a-104">成功認可佇列之後，您將需要更新您要安裝之產品的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c242a-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="c242a-105">建議您等到所有必要的檔案複製作業順利完成後，再改變登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c242a-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="c242a-106">更新登錄的其中一種方式是呼叫 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) \_ ，並指定 SPINST INIFILES、SPINST \_ registry 或 SPINST \_ INI2REG 旗標。</span><span class="sxs-lookup"><span data-stu-id="c242a-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="c242a-107">您可以在 **SetupInstallFromInfSection** 的單一呼叫中結合這些旗標。</span><span class="sxs-lookup"><span data-stu-id="c242a-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="c242a-108">下列範例會使用 SPINST \_ ALL ^ SPINST 檔案 \_ 來表示函式應處理所有列出的作業（檔案作業除外）。</span><span class="sxs-lookup"><span data-stu-id="c242a-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="c242a-109">由於只有 INI、登錄和檔案作業會列在 [ **安裝** ] 區段中，因此這是指定函式應處理所有 INI 和登錄作業的速記方法。</span><span class="sxs-lookup"><span data-stu-id="c242a-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="c242a-110">下列範例示範如何使用 **SetupInstallFromINFSection** 函式來安裝登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c242a-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="c242a-111">在此範例中， *OwnerWindow* 是 **Null** ，因為只有檔案作業會產生對話方塊，因此不需要父視窗。</span><span class="sxs-lookup"><span data-stu-id="c242a-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="c242a-112">"MyInf" 是包含要處理之區段的 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="c242a-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="c242a-113">參數 "MySection" 指定要安裝的區段。</span><span class="sxs-lookup"><span data-stu-id="c242a-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="c242a-114">組合旗標 SPINST \_ 所有 ^ SPINST 檔案 \_ ，指定要處理的安裝作業，在此案例中為檔案作業以外的所有作業。</span><span class="sxs-lookup"><span data-stu-id="c242a-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="c242a-115">來源根路徑指定為 "A： \\ "。</span><span class="sxs-lookup"><span data-stu-id="c242a-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="c242a-116">因為未處理任何複製作業，所以未指定 *CopyFlags*、 *MsgHandler*、 *CoNtext*、 *DeviceInfoSet* 和 *DeviceInfoData* 參數。</span><span class="sxs-lookup"><span data-stu-id="c242a-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



