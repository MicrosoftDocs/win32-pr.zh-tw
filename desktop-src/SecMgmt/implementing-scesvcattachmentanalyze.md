---
description: 必須從安全性資料庫和服務中取出設定資訊，比較這兩組資訊，然後更新安全性資料庫的 [分析] 區段，並提供任何差異。
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: 執行 SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193893"
---
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="80d0d-103">執行 SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="80d0d-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="80d0d-104">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)函式必須從安全性資料庫和服務中取出設定資訊，比較這兩組資訊，然後更新安全性資料庫的 [分析] 區段，並提供任何差異。</span><span class="sxs-lookup"><span data-stu-id="80d0d-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="80d0d-105">您可以使用下列演算法來確定這一點。</span><span class="sxs-lookup"><span data-stu-id="80d0d-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="80d0d-106">**若要執行 SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="80d0d-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="80d0d-107">定義取出及設定安全性資訊和傳回碼所需的變數。</span><span class="sxs-lookup"><span data-stu-id="80d0d-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="80d0d-108">在回呼結構中呼叫 pfQueryInfo 回呼函式，以從安全性資料庫中取出設定資訊。</span><span class="sxs-lookup"><span data-stu-id="80d0d-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="80d0d-109">從服務中取出對應的資訊。</span><span class="sxs-lookup"><span data-stu-id="80d0d-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="80d0d-110">比較從服務中取出的設定資料與從安全性資料庫抓取的設定資料。</span><span class="sxs-lookup"><span data-stu-id="80d0d-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="80d0d-111">如果資訊不同，請在回呼結構中呼叫 pfSetInfo 回呼函式來更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="80d0d-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="80d0d-112">釋放用來取得資訊的所有緩衝區。</span><span class="sxs-lookup"><span data-stu-id="80d0d-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="80d0d-113">在回呼結構中呼叫 pfFreeInfo 回呼函式，以釋放用於傳回之資料庫資訊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="80d0d-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="80d0d-114">如果有任何訊息要將擴充功能新增至分析記錄檔，請在回呼結構中呼叫 pfLogInfo 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="80d0d-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="80d0d-115">傳回適當的 **SCESTATUS** 碼。</span><span class="sxs-lookup"><span data-stu-id="80d0d-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="80d0d-116">下列範例顯示一個可能的 [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)執行。</span><span class="sxs-lookup"><span data-stu-id="80d0d-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="80d0d-117">請注意，在此範例中，QueryConfigurationLine 和 CompareValue 函式會分別從服務查詢資訊，並將這些值與從安全性資料庫抓取的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="80d0d-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="80d0d-118">不會顯示這些函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="80d0d-118">The implementation of these functions is not shown.</span></span>


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
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
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



