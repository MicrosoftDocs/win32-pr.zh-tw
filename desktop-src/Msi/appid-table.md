---
description: AppId 資料表或登錄表指定安裝程式在安裝期間設定並註冊 DCOM 伺服器，以執行下列其中一項動作。
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppId 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a121e6252c6054d5ac2765a9649e345035dde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882216"
---
# <a name="appid-table"></a>AppId 資料表

AppId 資料表或登錄 [表](registry-table.md) 指定安裝程式在安裝期間設定並註冊 DCOM 伺服器，以執行下列其中一項動作。

-   在與啟用伺服器的使用者不同的身分識別下執行 DCOM 伺服器。 例如，將 DCOM 伺服器設定為一律以互動式使用者或預先定義使用者的形式執行。
-   以服務形式執行 DCOM 伺服器。
-   設定 DCOM 伺服器的預設安全性存取權。
-   註冊 DCOM 伺服器，使其在不同的電腦上啟用。

此資料表會在與 [類別] 資料表的 [元件] 資料行中 DCOM 伺服器相關聯的元件安裝時進行處理 \_ 。 [](class-table.md) 未公告 AppId。

AppId 資料表具有下列資料行。



| Column               | 類型                       | 答案 | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | Y   | N        |
| RemoteServerName     | [格式 化](formatted.md) | N   | Y        |
| LocalService         | [Text](text.md)           | N   | Y        |
| ServiceParameters    | [Text](text.md)           | N   | Y        |
| DllSurrogate         | [Text](text.md)           | N   | Y        |
| ActivateAtStorage    | [整數](integer.md)     | N   | Y        |
| RunAsInteractiveUser | [整數](integer.md)     | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId
</dt> <dd>

[類別資料表](class-table.md)的 appid 資料行是 appid 資料表中這個資料行的外鍵。 此資料行包含 AppId 值，將會以 CLSID 撰寫，並在 HKCR appid 下建立 AppId GUID 金鑰 \\ 。

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

此資料行包含 "RemoteServerName" = xxxx 的 &lt; 值 &gt; ，將會寫入 HKCR \\ AppID \\ {AppID} \\ 。

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

此資料行包含 LocalService 的值，此值將會寫入 HKCR \\ AppID \\ { &lt; AppID &gt; } "LocalService" = &lt; xxx &gt; 。

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

此資料行包含將在 HKCR \\ AppID \\ {AppID>} "ServiceParameters" 下寫入的 ServiceParameters 值。

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

此資料行包含 DllSurrogate 的值，此值將會寫入 HKCR \\ AppId \\ { &lt; AppId &gt; } "DllSurrogate" = &lt; xxx &gt; 。 如果此資料行存在，則通常會是空字串。

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

此欄位中的非零整數值會導致 Windows Installer 將 HKCR \\ AppID \\ { &lt; AppID &gt; } "ActivateAtStorage" = "Y" 寫入登錄中。 如果欄位是空的，或值為零，則不會寫入任何值。

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

此欄位中的非零整數值會導致 Windows Installer 將 HKCR \\ AppID \\ {AppID>} "RunAs" = "Interactive User" 寫入登錄中。 如果欄位是空的，或值為零，則不會寫入任何值。

</dd> </dl>

## <a name="remarks"></a>備註

[RegisterClassInfo 動作](registerclassinfo-action.md)和[UnregisterClassInfo 動作](unregisterclassinfo-action.md)會使用此資料表。

請注意，AppId 資料表沒有註冊預設名稱的資料行。 因此，如果您需要撰寫使用者易記名稱做為預設的名稱值，就必須使用登錄 [資料表](registry-table.md)進行註冊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



