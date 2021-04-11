---
description: 下列程式提供組建程式的簡短總覽。
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: 建立 ISO7816-4 APDU 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191736"
---
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="ccf0f-103">建立 ISO7816-4 APDU 命令</span><span class="sxs-lookup"><span data-stu-id="ccf0f-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="ccf0f-104">若要將功能新增至服務提供者，您必須知道如何在基底服務提供者 Dll 內建立 ISO7816-4 [*應用程式協定資料單位*](/windows/desktop/SecGloss/a-gly) (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="ccf0f-105">下列程式提供組建程式的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="ccf0f-106">此處所包含的範例不一定是完整的;如需詳細資訊，請參閱範例應用程式和 Dll。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="ccf0f-107">**若要建立 ISO7816-4 APDU 命令**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="ccf0f-108">建立 [**ISCardCmd**](iscardcmd.md) 物件和 [**ISCardISO7816**](iscardiso7816.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    <span data-ttu-id="ccf0f-109">[**ISCardCmd**](iscardcmd.md)介面包含兩個 **IByteBuffer** 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="ccf0f-110">其中一個緩衝區包含實際的 APDU 命令字串 (加上任何要與命令) 傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="ccf0f-111">另一個則包含執行命令之後，卡片所傳回的任何回復資訊。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="ccf0f-112">使用這些物件，建立有效的 ISO7816-4 命令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ccf0f-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="ccf0f-113">以下是在 [**GetChallenge**](iscardiso7816-getchallenge.md) 方法中使用的程式碼：</span><span class="sxs-lookup"><span data-stu-id="ccf0f-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    <span data-ttu-id="ccf0f-114">[**ISCardISO7816：： GetChallenge**](iscardiso7816-getchallenge.md)方法會使用 [**ISCardCmd：： BuildCmd**](iscardcmd-buildcmd.md)方法來建立要求的 APDU。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="ccf0f-115">完成此動作的方式是在下列語句中，將適當的資訊寫入 [**ISCardCmd**](iscardcmd.md) APDU 緩衝區：</span><span class="sxs-lookup"><span data-stu-id="ccf0f-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="ccf0f-116">使用內建的 [**ISCardCmd**](iscardcmd.md) 物件、使用卡片進行交易、解讀結果，然後繼續。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="ccf0f-117">擴充超過 ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="ccf0f-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="ccf0f-118">展開上述服務提供者組建/執行程式的建議方式是建立新的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="ccf0f-119">這個 COM 物件應支援允許建立非 ISO7816-4 命令的新介面，而且應該匯總 [**ISCardISO7816**](iscardiso7816.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="ccf0f-120">建立 ISO7816-4 APDU 命令的範例</span><span class="sxs-lookup"><span data-stu-id="ccf0f-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="ccf0f-121">下列範例顯示上述程式中使用的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ccf0f-121">The following example shows the code used in the procedure above.</span></span>


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
