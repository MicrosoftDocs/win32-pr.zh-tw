---
description: 採用一組提供的設定資訊作為參數。
ms.assetid: 3c0a71f6-f643-4a5e-8b5c-15c976a3736e
title: 執行 SceSvcAttachmentUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381a2b04b75399b5f580426d9f2dd9f5911f52d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996753"
---
# <a name="implementing-scesvcattachmentupdate"></a><span data-ttu-id="8b559-103">執行 SceSvcAttachmentUpdate</span><span class="sxs-lookup"><span data-stu-id="8b559-103">Implementing SceSvcAttachmentUpdate</span></span>

<span data-ttu-id="8b559-104">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)函式會以一組提供的設定資訊作為參數。</span><span class="sxs-lookup"><span data-stu-id="8b559-104">The [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md) function takes as a parameter a set of supplied configuration information.</span></span> <span data-ttu-id="8b559-105">然後，它會從安全性資料庫抓取資訊、使用提供的設定資訊來計算新的基底設定、根據資料庫資訊和所提供的設定資訊來計算新的分析資訊，以及使用新的基本設定和分析資訊來更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="8b559-105">It then retrieves information from the security database, computes a new base configuration using the supplied configuration information, computes new analysis information based on the database information and the supplied configuration information, and updates the database with new base configuration and analysis information.</span></span> <span data-ttu-id="8b559-106">您可以使用下列演算法來執行 **SceSvcAttachmentUpdate** 。</span><span class="sxs-lookup"><span data-stu-id="8b559-106">You can implement **SceSvcAttachmentUpdate** by using the following algorithm.</span></span>

<span data-ttu-id="8b559-107">**若要執行 SceSvcAttachmentUpdate**</span><span class="sxs-lookup"><span data-stu-id="8b559-107">**To implement SceSvcAttachmentUpdate**</span></span>

1.  <span data-ttu-id="8b559-108">定義取出資訊、設定資訊和傳回碼所需的變數。</span><span class="sxs-lookup"><span data-stu-id="8b559-108">Define the variables needed to retrieve information, set information, and return codes.</span></span>
2.  <span data-ttu-id="8b559-109">在回呼結構中呼叫 pfQueryInfo 回呼函式，以從安全性資料庫中取出目前的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="8b559-109">Call the pfQueryInfo callback function in the callback structure to retrieve the current configuration information from the security database.</span></span>
3.  <span data-ttu-id="8b559-110">比較值：</span><span class="sxs-lookup"><span data-stu-id="8b559-110">Compare the values:</span></span>

    -   <span data-ttu-id="8b559-111">如果資料不同，請在回呼結構中呼叫 pfSetInfo 回呼函數，以更新資料庫中的設定資料。</span><span class="sxs-lookup"><span data-stu-id="8b559-111">If the data differs, call the pfSetInfo callback function in the callback structure to update the configuration data in the database.</span></span>
    -   <span data-ttu-id="8b559-112">如果資料相同，請在回呼結構中呼叫 pfSetInfo 回呼函數，以更新資料庫中的分析資料。</span><span class="sxs-lookup"><span data-stu-id="8b559-112">If the data is the same, call the pfSetInfo callback function in the callback structure to update the analysis data in the database.</span></span>

4.  <span data-ttu-id="8b559-113">重複直到所有資料都經過處理。</span><span class="sxs-lookup"><span data-stu-id="8b559-113">Repeat until all data is processed.</span></span>

<span data-ttu-id="8b559-114">下列範例顯示一個可能的 [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)執行。</span><span class="sxs-lookup"><span data-stu-id="8b559-114">The following example shows one possible implementation of [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md).</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo,
    IN SCESVC_CONFIGURATION_INFO *ServiceInfo
)
{
 
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ||
         ServiceInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }
  
  
    ////////////////////////////////////////////////////
    // Process supplied configuration information. 
    ////////////////////////////////////////////////////
    for (int i = 0; i < ServiceInfo->Count; i++)
    {
        retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              ServiceInfo->Line[I].Key,
                              TRUE,
                              (PVOID *)&pConfigInfo,
                              &EnumContext
                              );
        if(retCode != SCESTATUS_SUCCESS && 
           retCode != SCESTATUS_RECORD_NOT_FOUND)
        {
            ////////////////////////////////////////////////
            // Add code to handle errors
            ////////////////////////////////////////////////
            break;
        }
    
        //////////////////////////////////////////////////
        // If the supplied key is NULL, delete corresponding
        // key from configuration information and update 
        // analysis information if needed.
        //////////////////////////////////////////////////
        if(ServiceInfo->Line[I].Value == NULL)
        {
            if(retCode == SCESTATUS_SUCCESS)
            {
                EnumContext = 0;
                retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          ServiceInfo->Line [i].Key,
                                          TRUE,
                                          (PVOID *)&pAnalInfo,
                                          &EnumContext
                                          );
                if(retCode == SCESTATUS_RECORD_NOT_FOUND)
                {
                  ////////////////////////////////////////////
                  // Analysis information for key was not found.
                  // Update analysis information to include 
                  // deleted key.
                  /////////////////////////////////////////////
                  UpdateInfo->Count = 1;
                  UpdateInfo->Line = &UpdateLine;
                  UpdateLine.Key = pConfigInfo->Line[0].Key;
                  UpdateLine.Value = (PBYTE)pConfigInfo->Line[0].Value;
                  retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHandle,
                                          SceSvcAnalysisInfo,
                                          NULL,
                                          TRUE,
                                          &UpdateInfo
                                          );
                  if(retCode != SCESTATUS_SUCCESS)
                  {
                    //////////////////////////////////////////
                    // Add code for error return codes.
                    //////////////////////////////////////////
                  } 
                }
                else if (retCode == SCESTATUS_SUCCESS)
                {
                 ////////////////////////////////////////////
                 // Add code to delete configuration (analysis
                 // information is already in place.
                 ////////////////////////////////////////////
                }
                else
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
            
                //////////////////////////////////////////////
                // Delete key.
                //////////////////////////////////////////////
                retCode = (*(pSceCbInfo->pfSetInfo))( pSceCbInfo->sceHanlde,
                                        SceSvcConfigurationInfo,
                                        ServiceInfo->Line[I].Key,
                                        TRUE,
                                        NULL
                                        );
                if(retCode != SCESTATUS_SUCCESS)
                {
                  //////////////////////////////////////////
                  // Add code for error return codes.
                  //////////////////////////////////////////
                }
      
            }
            else
            {
                 /////////////////////////////////////////////////
                 // Supplied value is non-NULL; therefore. compare
                 // with current analysis information. If both are
                 // the same, delete current analysis. If they are 
                 // not the same, update security database with new
                 // value.
                 //////////////////////////////////////////
             
            }
   
   
           //////////////////////////////////////////////////
           // Free data returned.
           /////////////////////////////////////////////////
         (*(pSceCbInfo->pfFreeInfo))(pConfigInfo);
           pConfigInfo = NULL;
           
         (*(pSceCbInfo->pfSetInfo))(pAnalInfo);
           pAnalInfo = NULL;
          
          
          ////////////////////////////////////////////////////
          // Add code for other return codes if retCode is 
          // not SCESTATUS_SUCCESS.
          ///////////////////////////////////////////////////
          return retCode;
        }
    }
}
```



 

 



