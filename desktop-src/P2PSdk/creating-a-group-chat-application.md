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
# <a name="creating-a-group-chat-application"></a>建立群組聊天應用程式

本主題提供使用對等群組 API 開發聊天應用程式之主要步驟的相關程式碼範例，並提供每個 API 呼叫的內容。 不包含 UI 行為和整體應用程式結構。

> [!Note]  
> 對等 SDK 中提供完整的對等群組聊天範例應用程式。 本主題參考範例中提供的函式。

 

## <a name="initializing-a-group"></a>初始化群組

建立聊天應用程式的第一個步驟是呼叫具有最高支援版本的 [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) ，以初始化對等群組基礎結構。 在此情況下， **對等 \_ 群組 \_ 版本** 將會定義在應用程式標頭檔中。 基礎結構實際支援的版本會在 **peerVersion** 中傳回。


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>建立群組

如果沒有可加入的群組，或應用程式使用者想要建立一個新的群組，聊天應用程式必須能夠建立對等群組。 若要這樣做，您必須建立 [**對等 \_ 群組 \_ 屬性**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) 結構，並在其中填入群組的初始設定，包括對等群組的分類器、易記名稱、建立者的對等名稱，以及存在存留期。 填入此結構之後，您就可以將它傳遞至 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)。


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



## <a name="issuing-invitations"></a>發出邀請

發出邀請時，必須取得受邀者的 GMCs。 您可以藉由在受邀者上呼叫 [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) 及其身分識別名稱來取得這些資訊。 如果成功，就會將身分識別資訊 (含有 RSA 公開金鑰的64編碼憑證的 XML) 寫入至 (檔案的外部位置，在此範例中，您可以在此範例) 邀請者可以取得該檔案，並使用它來建立邀請。

此時，必須建立將邀請傳遞給受邀者的機制。 這可以是電子郵件或其他安全的檔案交換方法。 在下列範例中，會將邀請寫入檔案，然後傳送到受邀者的電腦。


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



邀請（例如身分識別）也會在外部發出。 在此範例中，邀請會以 **fputws** 的方式寫入檔案，其中受邀者可以取得該檔案，並在呼叫 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)時使用它。


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



## <a name="joining-a-peer-group"></a>加入對等群組

如果對等嘗試加入其他對等所建立的對等群組，它將需要該對等的邀請。 邀請是由外部進程或應用程式傳送給受邀者，並儲存至本機檔案（在下列範例中指定為 *pwzFileName*）。 邀請 XML blob 會從檔案讀取至 **wzInvitation** ，並傳遞至 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)。


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



## <a name="register-for-peer-events"></a>註冊對等事件

在連接之前，您應該註冊與應用程式相關的每一個對等事件。 在下列範例中，您會註冊下列事件：

-   對等 \_ 群組 \_ 事件 \_ 記錄 \_ 已變更。 由於記錄將用來包含公用聊天訊息，因此每次加入新的應用程式時，都必須通知應用程式。 收到此對等事件時，事件資料會以聊天訊息公開記錄。 應用程式應該只註冊它們想要直接處理的記錄類型。
-   對等 \_ 群組 \_ 事件 \_ 成員 \_ 已變更。 當成員加入或離開對等群組時，必須通知應用程式，讓參與者清單可以據以更新。
-   對等 \_ 群組 \_ 事件 \_ 狀態 \_ 已變更。 對等群組狀態的變更必須傳達給應用程式。 當對等群組成員的狀態指出它已連接到群組、與對等群組記錄資料庫進行同步處理，並主動接聽記錄更新時，才會將對等群組成員視為可在對等群組中使用。
-   對等 \_ 群組 \_ 事件 \_ 直接 \_ 連接。 您必須透過直接連接來執行兩個成員和資料交換之間的私用訊息，讓應用程式必須能夠處理直接連接要求。
-   對等 \_ 群組 \_ 事件 \_ 傳入 \_ 資料。 開始直接連線之後，此對等事件會對應用程式發出私用訊息的警示。


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



## <a name="connecting-to-a-peer-group"></a>連接至對等群組

建立或加入群組，並註冊適當的事件之後，就可以開始進行，並開始一個主動式聊天會話。 若要這樣做，請呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) ，然後傳入從 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) 或 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)取得的群組控制碼。 在呼叫之後，將會收到交談訊息做為對等 \_ 群組 \_ 事件 \_ 記錄 \_ 變更事件。

## <a name="obtaining-a-list-of-peer-group-members"></a>取得對等群組成員的清單

取得連接至對等群組的成員清單很簡單：呼叫 [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) 以抓取群組成員清單，然後反復呼叫 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) ，直到所有成員都被抓取為止。 您應該在處理每個成員結構之後呼叫 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) ，而且必須在處理完成時呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) 來關閉列舉。


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



## <a name="sending-a-chat-message"></a>傳送聊天訊息

在此範例中，會將交談訊息放在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record)結構的 **資料** 欄位中，藉以傳送聊天訊息。 記錄會藉由呼叫 [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)加入至對等群組記錄，此記錄會將它發佈，並 \_ \_ \_ \_ 在參與對等群組的所有對等上引發對等群組事件記錄變更事件。


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



## <a name="receiving-a-chat-message"></a>接收聊天訊息

若要接收聊天訊息，請針對對等群組事件記錄變更事件建立回呼函式，以 \_ \_ \_ \_ 呼叫類似下面的函式。 藉 [**由呼叫回檔**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) 函式中 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) 的先前呼叫所收到的事件資料來取得記錄。 聊天訊息會儲存在此記錄的 **資料** 欄位中。


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



 

 



