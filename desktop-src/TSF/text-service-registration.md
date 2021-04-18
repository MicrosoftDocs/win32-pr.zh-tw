---
title: 文字服務註冊
description: 除了標準的 COM 同進程伺服器登錄專案之外，文字服務還必須向文字服務架構 (TSF) 登錄，才能讓它與應用程式搭配使用。
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- 文字服務架構 (TSF) ，註冊
- TSF (文字服務架構) ，註冊
- 文字服務，註冊
- 文字服務架構 (TSF) ，語言設定檔
- TSF (文字服務架構) ，語言設定檔
- 文字服務，語言設定檔
- 文字服務架構 (TSF) 、類別目錄
- TSF (文字服務架構) 、類別
- 文字服務、類別
- 註冊文字服務
- 註冊語言設定檔
- 註冊類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463400"
---
# <a name="text-service-registration"></a>文字服務註冊

除了標準的 COM 同進程伺服器登錄專案之外，文字服務還必須向文字服務架構 (TSF) 登錄，才能讓它與應用程式搭配使用。 TSF 會提供 [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) 和 [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) 介面，以簡化註冊程式。

文字服務提供者也應提供數位簽章給其二進位可執行檔。 請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))。

## <a name="registering-the-text-service"></a>註冊文字服務

文字服務會以文字服務的類別識別碼呼叫 [ITfInputProcessorProfiles：： Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) ，向 TSF 註冊本身。 **ITfInputProcessorProfiles** 介面的實例是藉由使用 CLSID TF InputProcessorProfiles 呼叫 **CoCreateInstance** 取得的 \_ \_ 。

下列範例示範如何建立 **ITfInputProcessorProfiles** 物件並註冊文字服務。


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[ITfInputProcessorProfiles：：取消註冊](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>註冊語言設定檔

只有當應用程式具有焦點且在語言列中選取了適當的語言時，才可使用文字服務。 為了方便這項工作，TSF 需要文字服務為其支援的所有語言註冊本身。 文字服務會藉由呼叫 [ITfInputProcessorProfiles：： AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) 與文字服務類別識別碼、設定檔的語言識別項，以及識別語言設定檔的文字服務定義 **GUID** ，來註冊其語言設定檔。

您可以藉由呼叫 [ITfInputProcessorProfiles：： RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile)來移除語言設定檔。 **ITfInputProcessorProfiles：：取消註冊** 會移除文字服務的所有語言設定檔;當文字服務卸載時，需要移除個別的語言設定檔。

## <a name="registering-categories"></a>註冊類別

文字服務也必須註冊套用文字服務的類別。 例如，如果文字服務提供顯示內容資訊，則必須透過呼叫 [ITfCategoryMgr：： RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) 與第一個參數的文字服務的類別識別碼、GUID TFCAT DISPLAYATTRIBUTEPROVIDER 做為第二個參數 \_ \_ 以及第三個參數的文字服務類別識別碼，將本身註冊為顯示內容提供者。 可能的類別會列在 [預先定義的類別目錄值](predefined-category-values.md)底下。

藉由呼叫 [ITfCategoryMgr：： UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory)來移除先前註冊的類別。 ITfInputProcessorProfiles：：取消註冊會移除文字服務的所有類別;當文字服務卸載時，它必須移除個別類別。

 

 