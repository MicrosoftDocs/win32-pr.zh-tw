---
description: 定義可以用來連接到服務的端點類型。
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: 'UpdateEndpointType 列舉 (UpdateEndpointAuth) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510953"
---
# <a name="updateendpointtype-enumeration"></a>UpdateEndpointType 列舉

定義可以用來連接到服務的端點類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

用來連線到更新服務的用戶端伺服器端點，例如公司環境中的 Windows Update、Microsoft Update 和 WSUS 伺服器，以尋找可能適用于電腦之更新的相關資訊。

更新服務會傳回上次用戶端與伺服器同步處理後，已發行、修改或撤銷之更新的資訊。

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

當用戶端報告掃描、下載及安裝回更新服務的結果時，所使用的報告端點。

在公用服務 (Windows Update 和 Microsoft Update) 的情況下，這是為了品質監視用途所進行。

在私人服務（例如公司 WSUS 伺服器）的情況下，thhis 類型的端點也可讓伺服器收集有關受管理之用戶端電腦的清查和其他資訊。

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

當用戶端電腦連線到更新服務以查看是否有新版本的 Windows Update 代理程式用戶端軟體時，所使用的自我更新端點。

自我更新端點會使用不同的通訊協定，然後是 Client-Server 端點，因此即使發生錯誤狀況，可能會導致正常的用戶端伺服器同步處理無法在特定用戶端電腦上運作，也可以散發自我更新。

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

當用戶端電腦聯絡規定服務，以處理適用于目的電腦的特定更新時，所使用的法規端點。

法規服務可以指出更新是否「受管制」 (也稱為「節流」 ) -換句話說，法規服務可以告訴用戶端電腦它不應該對特定的更新採取任何動作，即使該更新看似適用也一樣。

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

只搭配私人服務使用的簡單目標端點， (在公司環境中) 的 WSUS 伺服器。 在公司環境中，可以將用戶端電腦指派給特定的目標群組，而且可以核准在某些群組的電腦上安裝更新，而不是其他群組的電腦。

例如，WSUS 系統管理員可能會為用來測試新更新的電腦建立「測試」群組，而系統管理員可能會核准測試群組中電腦上安裝的新發行更新，而不會將它們核准用於組織中的其他電腦。 簡單的目標交換可用來讓用戶端電腦向 WSUS 伺服器註冊自己，並允許伺服器告訴用戶端電腦它所在的群組。

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

安全的用戶端-伺服器端點，可讓用戶端取得需要授權之應用程式的相關資訊，以便在用戶端電腦上使用這些應用程式。 此授權架構目前僅供 Windows 8 用來部署透過 Windows Store 取得的應用程式和更新。 Windows Update、Microsoft Update 或 WSUS 目前未使用安全的用戶端-伺服器端點。

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

用戶端會使用次要服務驗證端點來提供驗證，然後才能取得需要授權的應用程式資訊，以便在用戶端電腦上使用。 此授權架構目前僅供 Windows 8 用來部署透過 Windows Store 取得的應用程式和更新。 Windows Update、Microsoft Update 或 WSUS 目前未使用次要服務驗證端點。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |



 

 




