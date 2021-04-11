---
description: 本主題提供使用對等群組 API 開發聊天應用程式之主要步驟的相關程式碼範例，並提供每個 API 呼叫的內容。
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: 建立群組聊天應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319192"
---
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="a0d23-103">建立群組聊天應用程式</span><span class="sxs-lookup"><span data-stu-id="a0d23-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="a0d23-104">本主題提供使用對等群組 API 開發聊天應用程式之主要步驟的相關程式碼範例，並提供每個 API 呼叫的內容。</span><span class="sxs-lookup"><span data-stu-id="a0d23-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="a0d23-105">不包含 UI 行為和整體應用程式結構。</span><span class="sxs-lookup"><span data-stu-id="a0d23-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="a0d23-106">對等 SDK 中提供完整的對等群組聊天範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0d23-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="a0d23-107">本主題參考範例中提供的函式。</span><span class="sxs-lookup"><span data-stu-id="a0d23-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="a0d23-108">初始化群組</span><span class="sxs-lookup"><span data-stu-id="a0d23-108">Initializing a Group</span></span>

<span data-ttu-id="a0d23-109">建立聊天應用程式的第一個步驟是呼叫具有最高支援版本的 [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) ，以初始化對等群組基礎結構。</span><span class="sxs-lookup"><span data-stu-id="a0d23-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="a0d23-110">在此情況下， **對等 \_ 群組 \_ 版本** 將會定義在應用程式標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="a0d23-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="a0d23-111">基礎結構實際支援的版本會在 **peerVersion** 中傳回。</span><span class="sxs-lookup"><span data-stu-id="a0d23-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="a0d23-112">建立群組</span><span class="sxs-lookup"><span data-stu-id="a0d23-112">Creating a Group</span></span>

<span data-ttu-id="a0d23-113">如果沒有可加入的群組，或應用程式使用者想要建立一個新的群組，聊天應用程式必須能夠建立對等群組。</span><span class="sxs-lookup"><span data-stu-id="a0d23-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="a0d23-114">若要這樣做，您必須建立 [**對等 \_ 群組 \_ 屬性**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) 結構，並在其中填入群組的初始設定，包括對等群組的分類器、易記名稱、建立者的對等名稱，以及存在存留期。</span><span class="sxs-lookup"><span data-stu-id="a0d23-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="a0d23-115">填入此結構之後，您就可以將它傳遞至 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)。</span><span class="sxs-lookup"><span data-stu-id="a0d23-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a><span data-ttu-id="a0d23-116">發出邀請</span><span class="sxs-lookup"><span data-stu-id="a0d23-116">Issuing Invitations</span></span>

<span data-ttu-id="a0d23-117">發出邀請時，必須取得受邀者的 GMCs。</span><span class="sxs-lookup"><span data-stu-id="a0d23-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="a0d23-118">您可以藉由在受邀者上呼叫 [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) 及其身分識別名稱來取得這些資訊。</span><span class="sxs-lookup"><span data-stu-id="a0d23-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="a0d23-119">如果成功，就會將身分識別資訊 (含有 RSA 公開金鑰的64編碼憑證的 XML) 寫入至 (檔案的外部位置，在此範例中，您可以在此範例) 邀請者可以取得該檔案，並使用它來建立邀請。</span><span class="sxs-lookup"><span data-stu-id="a0d23-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="a0d23-120">此時，必須建立將邀請傳遞給受邀者的機制。</span><span class="sxs-lookup"><span data-stu-id="a0d23-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="a0d23-121">這可以是電子郵件或其他安全的檔案交換方法。</span><span class="sxs-lookup"><span data-stu-id="a0d23-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="a0d23-122">在下列範例中，會將邀請寫入檔案，然後傳送到受邀者的電腦。</span><span class="sxs-lookup"><span data-stu-id="a0d23-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



<span data-ttu-id="a0d23-123">邀請（例如身分識別）也會在外部發出。</span><span class="sxs-lookup"><span data-stu-id="a0d23-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="a0d23-124">在此範例中，邀請會以 **fputws** 的方式寫入檔案，其中受邀者可以取得該檔案，並在呼叫 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)時使用它。</span><span class="sxs-lookup"><span data-stu-id="a0d23-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a><span data-ttu-id="a0d23-125">加入對等群組</span><span class="sxs-lookup"><span data-stu-id="a0d23-125">Joining a Peer Group</span></span>

<span data-ttu-id="a0d23-126">如果對等嘗試加入其他對等所建立的對等群組，它將需要該對等的邀請。</span><span class="sxs-lookup"><span data-stu-id="a0d23-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="a0d23-127">邀請是由外部進程或應用程式傳送給受邀者，並儲存至本機檔案（在下列範例中指定為 *pwzFileName*）。</span><span class="sxs-lookup"><span data-stu-id="a0d23-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="a0d23-128">邀請 XML blob 會從檔案讀取至 **wzInvitation** ，並傳遞至 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)。</span><span class="sxs-lookup"><span data-stu-id="a0d23-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a><span data-ttu-id="a0d23-129">註冊對等事件</span><span class="sxs-lookup"><span data-stu-id="a0d23-129">Register for Peer Events</span></span>

<span data-ttu-id="a0d23-130">在連接之前，您應該註冊與應用程式相關的每一個對等事件。</span><span class="sxs-lookup"><span data-stu-id="a0d23-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="a0d23-131">在下列範例中，您會註冊下列事件：</span><span class="sxs-lookup"><span data-stu-id="a0d23-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="a0d23-132">對等 \_ 群組 \_ 事件 \_ 記錄 \_ 已變更。</span><span class="sxs-lookup"><span data-stu-id="a0d23-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="a0d23-133">由於記錄將用來包含公用聊天訊息，因此每次加入新的應用程式時，都必須通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0d23-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="a0d23-134">收到此對等事件時，事件資料會以聊天訊息公開記錄。</span><span class="sxs-lookup"><span data-stu-id="a0d23-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="a0d23-135">應用程式應該只註冊它們想要直接處理的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="a0d23-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="a0d23-136">對等 \_ 群組 \_ 事件 \_ 成員 \_ 已變更。</span><span class="sxs-lookup"><span data-stu-id="a0d23-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="a0d23-137">當成員加入或離開對等群組時，必須通知應用程式，讓參與者清單可以據以更新。</span><span class="sxs-lookup"><span data-stu-id="a0d23-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="a0d23-138">對等 \_ 群組 \_ 事件 \_ 狀態 \_ 已變更。</span><span class="sxs-lookup"><span data-stu-id="a0d23-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="a0d23-139">對等群組狀態的變更必須傳達給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0d23-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="a0d23-140">當對等群組成員的狀態指出它已連接到群組、與對等群組記錄資料庫進行同步處理，並主動接聽記錄更新時，才會將對等群組成員視為可在對等群組中使用。</span><span class="sxs-lookup"><span data-stu-id="a0d23-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="a0d23-141">對等 \_ 群組 \_ 事件 \_ 直接 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="a0d23-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="a0d23-142">您必須透過直接連接來執行兩個成員和資料交換之間的私用訊息，讓應用程式必須能夠處理直接連接要求。</span><span class="sxs-lookup"><span data-stu-id="a0d23-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="a0d23-143">對等 \_ 群組 \_ 事件 \_ 傳入 \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="a0d23-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="a0d23-144">開始直接連線之後，此對等事件會對應用程式發出私用訊息的警示。</span><span class="sxs-lookup"><span data-stu-id="a0d23-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="a0d23-145">連接至對等群組</span><span class="sxs-lookup"><span data-stu-id="a0d23-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="a0d23-146">建立或加入群組，並註冊適當的事件之後，就可以開始進行，並開始一個主動式聊天會話。</span><span class="sxs-lookup"><span data-stu-id="a0d23-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="a0d23-147">若要這樣做，請呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) ，然後傳入從 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) 或 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)取得的群組控制碼。</span><span class="sxs-lookup"><span data-stu-id="a0d23-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="a0d23-148">在呼叫之後，將會收到交談訊息做為對等 \_ 群組 \_ 事件 \_ 記錄 \_ 變更事件。</span><span class="sxs-lookup"><span data-stu-id="a0d23-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="a0d23-149">取得對等群組成員的清單</span><span class="sxs-lookup"><span data-stu-id="a0d23-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="a0d23-150">取得連接至對等群組的成員清單很簡單：呼叫 [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) 以抓取群組成員清單，然後反復呼叫 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) ，直到所有成員都被抓取為止。</span><span class="sxs-lookup"><span data-stu-id="a0d23-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="a0d23-151">您應該在處理每個成員結構之後呼叫 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) ，而且必須在處理完成時呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) 來關閉列舉。</span><span class="sxs-lookup"><span data-stu-id="a0d23-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a><span data-ttu-id="a0d23-152">傳送聊天訊息</span><span class="sxs-lookup"><span data-stu-id="a0d23-152">Sending a Chat Message</span></span>

<span data-ttu-id="a0d23-153">在此範例中，會將交談訊息放在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)結構的 **資料** 欄位中，藉以傳送聊天訊息。</span><span class="sxs-lookup"><span data-stu-id="a0d23-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="a0d23-154">記錄會藉由呼叫 [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)加入至對等群組記錄，此記錄會將它發佈，並 \_ \_ \_ \_ 在參與對等群組的所有對等上引發對等群組事件記錄變更事件。</span><span class="sxs-lookup"><span data-stu-id="a0d23-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a><span data-ttu-id="a0d23-155">接收聊天訊息</span><span class="sxs-lookup"><span data-stu-id="a0d23-155">Receiving a Chat Message</span></span>

<span data-ttu-id="a0d23-156">若要接收聊天訊息，請針對對等群組事件記錄變更事件建立回呼函式，以 \_ \_ \_ \_ 呼叫類似下面的函式。</span><span class="sxs-lookup"><span data-stu-id="a0d23-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="a0d23-157">藉 [**由呼叫回檔**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) 函式中 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) 的先前呼叫所收到的事件資料來取得記錄。</span><span class="sxs-lookup"><span data-stu-id="a0d23-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="a0d23-158">聊天訊息會儲存在此記錄的 **資料** 欄位中。</span><span class="sxs-lookup"><span data-stu-id="a0d23-158">The chat message is stored in the **data** field of this record.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



