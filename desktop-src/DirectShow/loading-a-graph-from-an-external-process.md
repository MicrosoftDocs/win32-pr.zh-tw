---
description: 從外部進程載入圖形
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: 從外部進程載入圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560161"
---
# <a name="loading-a-graph-from-an-external-process"></a>從外部進程載入圖形

GraphEdit 可以載入外部進程所建立的篩選圖形。 使用這項功能，您可以查看應用程式所建立的篩選圖形，而且您的應用程式中只會有少量的額外程式碼。

> [!Note]  
> 這項功能需要 Windows 2000、Windows XP 或更新版本。

 

> [!Note]  
> 從 Windows Vista 開始，您必須註冊 proppage.dll 以啟用這項功能。 Proppage.dll 包含在 Windows SDK 中。

 

應用程式必須在執行中的物件資料表中註冊篩選圖形實例， (的 ROT) 。 ROT 是可全域存取的查閱資料表，可追蹤正在執行的物件。 物件是在 ROT 中依標記註冊。 若要連接到圖形，GraphEdit 會在 ROT 搜尋其顯示名稱符合特定格式的名字：


```C++
!FilterGraph X pid Y
```



其中 *X* 是篩選圖形管理員的十六進位位址，而 *Y* 是處理序識別碼，也是十六進位。

當您的應用程式第一次建立篩選圖形時，請呼叫下列函數：


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



此函數會建立篩選圖形的標記和新的 ROT 專案。 第一個參數是篩選圖形的指標。 第二個參數會接收可識別新的 ROT 專案的值。 在應用程式釋放篩選圖形之前，呼叫下列函式以移除 ROT 專案。 *PdwRegister* 參數是 AddToRot 函數所傳回的識別碼。


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



下列程式碼範例顯示如何呼叫這些函式。 在此範例中，會有條件地編譯加入和移除 ROT 專案的程式碼，使其只包含在 debug 組建中。


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



若要在 GraphEdit 中查看篩選圖形，請同時執行您的應用程式和 GraphEdit。 在 **[GraphEdit 檔案** ] 功能表中，按一下 [連線 **到遠端圖形** ]。在 [ **連接到圖形** ] 對話方塊中，選取應用程式的處理序識別碼 (pid) ，然後按一下 **[確定]**。 GraphEdit 會載入篩選圖形並顯示它。 請勿在此圖形上使用任何其他 GraphEdit 功能，這可能會導致非預期的結果。 例如，不要新增或移除篩選，或停止和啟動圖形。 結束您的應用程式之前，請關閉 GraphEdit。

> [!Note]  
> 當您的應用程式結束時，可能會遇到各種判斷提示。 您可以忽略這些錯誤。

 

下圖顯示 [ **連接到圖形** ] 對話方塊。

![連接至圖形](images/gedit-spy.png)

當 GraphEdit 載入圖形時，它會在目標應用程式的內容中執行。 因此，GraphEdit 可能會封鎖，因為它正在等候執行緒。 例如，如果您在偵錯工具中逐步執行程式碼，就會發生這種情況。

這項功能僅適用于應用程式的 debug 組建，而非零售組建，因為它可讓其他應用程式查看或控制篩選圖形。

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>從命令列連接至遠端圖形

GraphEdit 支援命令列選項，可在啟動時自動載入遠端圖形。 語法為：


```C++
GraphEdt -a moniker
```



其中的 *名字* 標記是使用 AddToRot 函式建立的標記，如先前所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 GraphEdit 模擬圖表建立](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



