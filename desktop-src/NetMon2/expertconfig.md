---
description: EXPERTCONFIG 結構包含專家的設定資料。 專家將 RawConfigData 成員與專家特定的結構重迭。
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: 'EXPERTCONFIG 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 93b47054fd5b8103d5bbe0d762db87f285a5f01690d0b93f6da14d215e404a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366908"
---
# <a name="expertconfig-structure"></a>EXPERTCONFIG 結構

**EXPERTCONFIG** 結構包含專家的設定資料。 專家將 **RawConfigData** 成員與專家特定的結構重迭。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>成員

<dl> <dt>

**RawConfigLength**
</dt> <dd>

結構的總長度，包括用於成員的四個位元組。 當結構儲存至磁片磁碟機並從磁片磁碟機讀取時，網路監視器會使用此值。

</dd> <dt>

**RawConfigData**
</dt> <dd>

設定資料。 專家必須加入設定資料。 例如，假設您有一個看起來像這樣的資料結構。

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

請注意， **RawConfigLength** 可確保重迭的運作正常。 當您使用資料時，您的程式碼可能如下所示：

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




