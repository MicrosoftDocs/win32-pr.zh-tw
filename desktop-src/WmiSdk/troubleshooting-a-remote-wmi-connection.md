---
description: 下列各節描述開發人員建立遠端 WMI 連接時可能遇到的常見問題。
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: 疑難排解遠端 WMI 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312414"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>疑難排解遠端 WMI 連接

下列各節描述開發人員建立遠端 WMI 連接時可能遇到的常見問題。

本主題將討論下列各節：

-   [DCOM 拒絕存取](#dcom-access-denied)
-   [無法連線](#failure-to-connect)
-   [WMI 連接逾時](#wmi-connection-timed-out)
-   [相關主題](#related-topics)

## <a name="dcom-access-denied"></a>DCOM 拒絕存取

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀
</dt> <dd>

您的連接失敗，並出現「DCOM 拒絕存取」錯誤，以及十進位值-2147024891 或 hex value0x80070005。

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題
</dt> <dd>

DCOM 可能未設定為允許 WMI 連接。

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度
</dt> <dd>

您可以使用 [DCOM 設定公用程式] (**DCOMCnfg.exe**) 在 **主控台** 的 [系統 **管理工具**] 中找到，來設定 WMI 的 dcom 設定。 此公用程式會公開設定，讓某些使用者透過 DCOM 從遠端連線到電腦。 系統管理員群組的成員預設允許遠端連線到電腦。 您可以使用此公用程式來設定安全性，以啟動、存取及設定 WMI 服務。

如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。

</dd> </dl>

## <a name="failure-to-connect"></a>無法連線

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀
</dt> <dd>

您無法連接到遠端系統上的 WMI。

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題
</dt> <dd>

您可能嘗試連接到不支援 WMI 的系統。 不支援下列作業系統版本之間的連接：

-   您無法連接到執行 Starter、Basic 或 Home edition 的電腦。

或者，您可能嘗試連接到需要加密連接的命名空間，而該命名空間需要驗證層級 `pktPrivacy` 、 **WbemAuthenticationLevelPktPrivacy** 或 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度
</dt> <dd>

如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)、 [保護 c + + 用戶端和提供者](securing-c---clients-and-providers.md)，或 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>WMI 連接逾時

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>症狀
</dt> <dd>

您的 WMI 連接逾時。

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>問題
</dt> <dd>

由於網路延遲問題，電腦只是無法及時回應。

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>解析度
</dt> <dd>

當您透過呼叫 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 或 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)來連線到 WMI 時，可以將 **wbemConnectFlagUseMaxWait** 旗標 (腳本) 或 **WBEM 旗 \_ 標 \_ CONNECT \_ USE \_ MAX \_ WAIT** in c + + 值設定為 128 (0x80) 在呼叫上強加兩 (2) 分鐘的超時時間。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



