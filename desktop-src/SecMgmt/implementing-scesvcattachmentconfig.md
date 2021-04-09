---
description: 必須從安全性資料庫取出資訊，然後使用該資訊來設定服務。
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: 執行 SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944751"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="33921-103">執行 SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="33921-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="33921-104">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)函數必須從安全性資料庫取出資訊，然後使用該資訊來設定服務。</span><span class="sxs-lookup"><span data-stu-id="33921-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="33921-105">在執行 [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)時，您可以取出所有資訊，然後設定服務，或是在步驟中取得和設定服務。</span><span class="sxs-lookup"><span data-stu-id="33921-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="33921-106">下列演算法會抓取所有資訊，然後設定服務。</span><span class="sxs-lookup"><span data-stu-id="33921-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="33921-107">**若要執行 SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="33921-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="33921-108">定義取出資訊和傳回碼所需的變數。</span><span class="sxs-lookup"><span data-stu-id="33921-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="33921-109">在回呼結構中呼叫 pfQueryInfo 回呼函式，以從安全性資料庫中取出設定資訊。</span><span class="sxs-lookup"><span data-stu-id="33921-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="33921-110">使用傳回的資訊來設定系統。</span><span class="sxs-lookup"><span data-stu-id="33921-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="33921-111">在回呼結構中呼叫 pfFreeInfo 回呼函式，以釋放用於傳回之資訊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="33921-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="33921-112">如果有任何訊息要將擴充功能新增至分析記錄檔，請在回呼結構中呼叫 pfLogInfo 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="33921-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="33921-113">傳回適當的 **SCESTATUS** 碼。</span><span class="sxs-lookup"><span data-stu-id="33921-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="33921-114">下列範例顯示一個可能的 [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)執行。</span><span class="sxs-lookup"><span data-stu-id="33921-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="33921-115">請注意，在此範例中，函數 ProcessConfigurationLine 會設定服務設定。</span><span class="sxs-lookup"><span data-stu-id="33921-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="33921-116">未顯示此函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="33921-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
  ////////////////////////////////////////////////////
  // Define variables.
  ////////////////////////////////////////////////////
     PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
     SCESTATUS                      retCode;
     SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
     if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
     {
        return(SCESTATUS_INVALID_PARAMETER);
     }
  
  
      ////////////////////////////////////////////////////
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



