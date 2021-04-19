---
description: 當您的附件嵌入式管理單元延伸模組已將自己新增至 [服務] 節點之後，就應該與 [安全性設定] 嵌入式管理單元建立通訊。
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: 建立與設定嵌入式管理單元的通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998312"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>建立與設定嵌入式管理單元的通訊

當您的附件嵌入式管理單元延伸模組已將自己新增至 [服務] 節點之後，就應該與 [安全性設定] 嵌入式管理單元建立通訊。 這是必要的，因為附件嵌入式管理單元擴充功能會從 [安全性設定] 嵌入式管理單元取得其資料，以及使用者所做的任何變更。 您可以如下列程式所述完成此步驟。

**若要建立與安全性設定嵌入式管理單元的通訊**

1.  使用 CCF SCESVC 附件剪貼簿格式取得設定檔案名稱 \_ \_ ，此格式會將設定檔案名稱傳回為 **PWSTR**。

    如果附件是在 [設定類型] 節點下插入，則附件必須知道它的設定。  (它會在介面初始化期間，將這項資訊傳達給安全性設定嵌入式管理單元 ) 。在此情況下，請使用下列程式碼。

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  使用「安全性設定」嵌入式管理單元來設定內容。知道設定名稱之後，或如果服務節點是分析節點，則附件嵌入式管理單元擴充功能必須呼叫 [**ISceSvcAttachmentData：： Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) 來設定內容，如下列範例所示。

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> 當您完成使用 [**ISceSvcAttachmentData：： Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize)傳回的控制碼時，請呼叫 [**ISceSvcAttachmentData：： CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) 函式來關閉控制碼。 這通常會在使用者關閉 MMC 主控台時完成。

 

 

 



