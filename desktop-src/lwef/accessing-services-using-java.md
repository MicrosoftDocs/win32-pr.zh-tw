---
title: 使用 JAVA 存取服務
description: 使用 JAVA 存取服務
ms.assetid: 3eced858-487a-4f36-a7a1-34ac827aad13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c24ae7508b5999e5d07f2480d49cb4c20dd89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933145"
---
# <a name="accessing-services-using-java"></a><span data-ttu-id="dd23d-103">使用 JAVA 存取服務</span><span class="sxs-lookup"><span data-stu-id="dd23d-103">Accessing Services Using Java</span></span>

<span data-ttu-id="dd23d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="dd23d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="dd23d-105">您也可以從 JAVA applet 存取 Microsoft Agent 服務。</span><span class="sxs-lookup"><span data-stu-id="dd23d-105">You can also access Microsoft Agent services from a Java applet.</span></span> <span data-ttu-id="dd23d-106">許多可透過 Microsoft Agent 介面存取的函式會透過傳址方式傳遞的參數傳回值。</span><span class="sxs-lookup"><span data-stu-id="dd23d-106">Many of the functions accessible through the Microsoft Agent interfaces return values through parameters passed by reference.</span></span> <span data-ttu-id="dd23d-107">若要從 JAVA 傳遞這些參數，您必須在程式碼中建立單一元素的陣列，並將它們以參數形式傳遞給適當的函式。</span><span class="sxs-lookup"><span data-stu-id="dd23d-107">In order to pass these parameters from Java, it is necessary to create single-element arrays in your code and pass them as parameters to the appropriate function.</span></span> <span data-ttu-id="dd23d-108">如果您使用 Microsoft Visual c + +，並已在 Microsoft 代理程式伺服器上執行 JAVA 類型程式庫嚮導，請參閱 summary.txt 檔案，以檢查哪些函數需要陣列引數。</span><span class="sxs-lookup"><span data-stu-id="dd23d-108">If you are using Microsoft Visual J++ and have run the Java Type Library Wizard on the Microsoft Agent server, refer to the summary.txt file to review which functions require array arguments.</span></span> <span data-ttu-id="dd23d-109">程式與 C 中的程式類似;您可以使用 [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) 介面來建立伺服器的實例，然後載入該字元：</span><span class="sxs-lookup"><span data-stu-id="dd23d-109">The procedure is similar to that in C; you use the [**IAgentEx**](https://www.bing.com/search?q=**IAgentEx**) interface to create an instance of the server, then load the character:</span></span>


```
private IAgentEx            m_AgentEx = null;
private IAgentCharacterEx   m_Merlin[] = {null};
private int                 m_MerlinID[] = {-1};
private int                 m_RequestID[] = {0};
private final String        m_CharacterPath = "merlin.acs";

public void start()
{
      // Start the Microsoft Agent Server

      m_AgentEx = (IAgentEx) new AgentServer();

      try
      {

         Variant characterPath = new Variant();
         characterPath.putString(m_CharacterPath);

         // Load the character

         m_AgentEx.Load(characterPath,
                    m_MerlinID,
                    m_RequestID);
      }
```



<span data-ttu-id="dd23d-110">從 HTTP 遠端位置（例如網站）載入字元時，此程式會稍有不同。</span><span class="sxs-lookup"><span data-stu-id="dd23d-110">The procedure is slightly different when loading characters from a HTTP remote location such as a website.</span></span> <span data-ttu-id="dd23d-111">在此情況下， [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) 方法是非同步，而且會引發 E \_ 暫止 (0X8000000A) 的 COM 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="dd23d-111">In this case the [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) method is asynchronous and will raise a COM exception of E\_PENDING (0x8000000a).</span></span> <span data-ttu-id="dd23d-112">您將需要攔截此例外狀況，並正確地處理它，就像在下列函式中所做的一樣：</span><span class="sxs-lookup"><span data-stu-id="dd23d-112">You will need to catch this exception and handle it correctly as is done in the following functions:</span></span>


```
// Constants used in asynchronous character loads

private final int E_PENDING = 0x8000000a;
private final int NOERROR = 0;


// This function loads a character from the specified path.
// It correctly handles the loading of characters from
// remote sites.

// This sample doesn't care about the request id returned
// from the Load call.  Real production code might use the
// request id and the RequestComplete callback to check for
// a successful character load before proceeding.

public int LoadCharacter(Variant path, int[] id)
{
   int requestid[] = {-1};
   int hRes = 0;

   try
   {
      // Load the character

      m_AgentEx.Load(path, id, requestid);
   }
   catch(com.ms.com.ComException e)
   {
      // Get the HRESULT

      hRes = e.getHResult();
      
      // If the error code is E_PENDING, we return NOERROR

      if (hRes == E_PENDING)
         hRes = NOERROR;
   }

   return hRes;
}

public void start()
{
   if (LoadCharacter(characterPath, m_MerlinID) != NOERROR)
   {
      stop();
      return;
   }

   // Other initialization code here

   .
   .
   .
}
```



<span data-ttu-id="dd23d-113">然後取得可讓您存取其方法的 [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) 介面：</span><span class="sxs-lookup"><span data-stu-id="dd23d-113">Then get the [**IAgentCharacterEx**](https://www.bing.com/search?q=**IAgentCharacterEx**) interface that enables you to access its methods:</span></span>


```
// Get the IAgentCharacterEx interface for the loaded
// character by passing its ID to the Agent server.

m_AgentEx.GetCharacterEx(m_MerlinID[0], m_Merlin);

// Show the character

m_Merlin[0].Show(FALSE, m_RequestID);

// And speak hello

m_Merlin[0].Speak("Hello World!", "", m_RequestID);
```



<span data-ttu-id="dd23d-114">同樣地，若要收到事件的通知，您必須執行 [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) 或 [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) 介面，建立並註冊該型別的物件：</span><span class="sxs-lookup"><span data-stu-id="dd23d-114">Similarly, to be notified of events, you must implement either the [**IAgentNotifySink**](https://www.bing.com/search?q=**IAgentNotifySink**) or the [**IAgentNotifySinkEx**](https://www.bing.com/search?q=**IAgentNotifySinkEx**) interface, creating and registering an object of that type:</span></span>


```
...
// Declare an Agent Notify Sink so that we can get
// notification callbacks from the Agent server.

private AgentNotifySinkEx m_SinkEx = null;
private int            m_SinkID[] = {-1};

public void start()
   {
   ...
   // Create and register a notify sink

   m_SinkEx = new AgentNotifySinkEx();

   m_AgentEx.Register(m_SinkEx, m_SinkID);
   …
   // Give our notify sink access to the character

   m_SinkEx.SetCharacter(m_Merlin[0]);
   ...
   }
```



<span data-ttu-id="dd23d-115">若要從 JAVA applet 存取 Microsoft 代理程式，您必須產生使用 applet 安裝的 JAVA 類別。</span><span class="sxs-lookup"><span data-stu-id="dd23d-115">In order to access Microsoft Agent from a Java applet, you must generate Java classes that you install with the applet.</span></span> <span data-ttu-id="dd23d-116">例如，您可以使用 Visual j + + JAVA 類型程式庫 Wizard 來產生這些檔案。</span><span class="sxs-lookup"><span data-stu-id="dd23d-116">You can use the Visual J++ Java Type Library Wizard, for example, to generate these files.</span></span> <span data-ttu-id="dd23d-117">如果您想要在網頁上裝載小程式，您必須建立一個帶正負號的 JAVA CAB，內含隨頁面下載的產生類別檔案。</span><span class="sxs-lookup"><span data-stu-id="dd23d-117">If you plan to host the applet on a webpage, you will need to build a signed Java CAB inclusive of the generated class files that download with the page.</span></span> <span data-ttu-id="dd23d-118">需要類別檔案才能存取 Microsoft 代理程式伺服器，因為它是在 JAVA 沙箱外部執行的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="dd23d-118">The class files are necessary to access the Microsoft Agent Server since it is a COM object, that executes outside of the Java sandbox.</span></span> <span data-ttu-id="dd23d-119">若要深入瞭解 JAVA 的 Trust-Based 安全性，請參閱 <https://www.microsoft.com/java/security> 。</span><span class="sxs-lookup"><span data-stu-id="dd23d-119">To learn more about Trust-Based Security for Java, see <https://www.microsoft.com/java/security>.</span></span>

 

 