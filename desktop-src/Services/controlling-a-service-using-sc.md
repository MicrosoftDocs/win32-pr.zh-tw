---
description: Windows SDK 包含可用於控制服務的命令列公用程式（Sc.exe）。 其命令會對應至 SCM 提供的函式。 語法如下所示。
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: 使用 SC 控制服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126448"
---
# <a name="controlling-a-service-using-sc"></a>使用 SC 控制服務

Windows SDK 包含可用於控制服務的命令列公用程式（Sc.exe）。 其命令會對應至 SCM 提供的函式。 語法如下所示。

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

<dl> <dd>continue</dd> <dd>控制</dd> <dd>審問</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

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

[服務控制要求](service-control-requests.md)
</dt> <dt>

[服務啟動](service-startup.md)
</dt> </dl>

 

 



