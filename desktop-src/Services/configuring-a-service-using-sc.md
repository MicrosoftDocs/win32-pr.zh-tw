---
description: Windows SDK 包含命令列公用程式（Sc.exe），可用來查詢或修改已安裝服務的資料庫。 其命令會對應至 SCM 提供的函式。 語法如下所示。
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: 使用 SC 設定服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 976eb5fb8e9a462e4d1de38413593343dd1d8624985593f6ecb9c691ae9670da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968225"
---
# <a name="configuring-a-service-using-sc"></a>使用 SC 設定服務

Windows SDK 包含命令列公用程式（Sc.exe），可用來查詢或修改已安裝服務的資料庫。 其命令會對應至 SCM 提供的函式。 語法如下所示。

## <a name="syntax"></a>Syntax

**sc** \[*ServerName* \]*命令* \[ \] ServiceName \[ \] option1 \[*option2* \]...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*
</dt> <dd>

選用的伺服器名稱。 使用表單 \\ \\ *ServerName*。

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*命令*
</dt> <dd>

下列其中一個命令：

<dl> <dd>boot</dd> <dd>config</dd> <dd>建立</dd> <dd>delete</dd> <dd>description</dd> <dd>EnumDepend</dd> <dd>失敗</dd> <dd>failureflag</dd> <dd>GetDisplayName</dd> <dd>GetKeyName</dd> <dd>鎖定</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>查詢</dd> <dd>queryex</dd> <dd>privs</dd> <dd>QueryLock</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>sidtype</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*
</dt> <dd>

安裝時所指定的服務名稱。

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*option1*
</dt> <dd>

選用參數。

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*option2*
</dt> <dd>

選用參數。

</dd> </dl>

## <a name="remarks"></a>備註

若要查看命令的完整語法，請使用下列命令：

**sc** *命令*

## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務組態](service-configuration.md)
</dt> <dt>

[服務安裝、移除和列舉](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



