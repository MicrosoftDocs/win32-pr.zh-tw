---
description: 不再支援 WMI 記錄檔。
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: 記錄 WMI 活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978230"
---
# <a name="logging-wmi-activity"></a>記錄 WMI 活動

不再支援 WMI 記錄檔。 從 Windows Vista 開始，WMI 會使用 [windows 的事件追蹤 (ETW](/windows/desktop/ETW/event-tracing-portal)) 以及透過 **事件檢視器** UI 或 Wevtutil 命令列工具提供的事件。 如需詳細資訊，請參閱 ETW 提供者和 [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) 命令列檔。

本主題將討論下列各節：

-   [Windows Vista 之前的 WMI 記錄檔](#wmi-log-files-before-windows-vista)
-   [Windows Vista 之前的 WMI 核心元件記錄活動](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Windows Vista 之前的 WMI 提供者元件記錄活動](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [相關主題](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>Windows Vista 之前的 WMI 記錄檔

WMI 和各種提供者所建立的記錄檔會記錄：事件、追蹤或診斷資料、錯誤和各種活動。 只有系統管理員才具有在% windir% \\ system32 wbem 記錄檔中找到之 WMI 記錄檔資料夾的讀取權限 \\ \\ 。

只有 WMI 核心元件或 WMI 提供者會寫入記錄檔。 您只能讀取或查看這些記錄檔中的資料，以供診斷之用。 您可以在 WMI 記錄檔目錄中建立並儲存自己的記錄檔。

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Windows Vista 之前的 WMI 核心元件記錄活動

這些檔案不包含適合以程式設計方式讀取的一致格式。 如需特定記錄檔的詳細資訊，請參閱 [WMI 記錄](wmi-log-files.md)檔。

設定下列登錄機碼時，會發生 WMI 核心元件的記錄活動：

-   記錄層級

    記錄層級登錄值的變更會立即生效。 不需要重新開機 WMI 服務。

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄**= 2

    下列清單列出可在登錄中定義的記錄層級。

    

    | 記錄層級 | 描述               |
    |---------------|---------------------------|
    | 0             | 無記錄                |
    | 1             | 只記錄錯誤           |
    | 2             | 詳細資訊記錄 (預設)  |

    

     

-   記錄檔位置

    若要讓記錄檔位置的變更生效，請重新開機 WMI 服務。

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄目錄**=% windir% \\ system32 \\ WBEM \\ 記錄

-   記錄檔大小上限（以位元組為單位）

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **記錄檔大小上限**= 65536

您可以透過登錄編輯程式或 Microsoft Management Console 的 WMI 嵌入式管理單元來變更這些登錄機碼值。

**在 Windows Vista 之前設定 WMI 的記錄層級**

1.  按一下 **[開始]** ，然後按一下 **[執行]** 。
2.  輸入 **wmimgmt.msc services.msc**
3.  在 [動作] 功能表上，按一下 [內容]。
4.  在 [ **記錄** ] 索引標籤上，將記錄層級設定為 **停用**、 **已啟用** 或 **詳細** 資訊。
5.  在 [ **位置：**] 中，輸入記錄檔資料夾的路徑，並以 **大小上限 (位元組) ：**，設定記錄檔的大小上限（以位元組為單位）。

如需有關設定記錄檔屬性的詳細資訊，請參閱 WMI 控制應用程式的線上說明。

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Windows Vista 之前的 WMI 提供者元件記錄活動

啟用 WMI 核心元件的記錄時，也會針對具有記錄功能的任何提供者啟用記錄。

下列清單列出必要的值。

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**檔**
</dt> <dd>

記錄檔的完整路徑和檔案名。 預設值為% windir% \\ system32 \\ wbem \\ 記錄。 必須將命名值的 **型** 別設定為 = File，才能使用此命名值。

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**水準**
</dt> <dd>

用來定義提供者所產生之偵錯工具輸出型別的32位邏輯遮罩。 此值與提供者相依。 預設值是 0 (零)。

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

記錄檔的檔案大小上限（以位元組為單位）。 這個整數值的範圍必須介於1024到 2 ^ 32-1 之間。 當檔案大小超過此值時，會將檔案重新命名為 **~ filename** ，並建立新的空白記錄檔。 記錄檔所需的磁碟空間是 **MaxFileSize** 值的兩倍。 預設值為65535。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**
</dt> <dd>

可以設定為 = File 或 = 偵錯工具。 如果設定為 = File，則會將追蹤資訊寫入名為的檔案中指定 **的記錄** 檔。 預設值為 = File。

</dd> </dl>

例如，若要從 View Provider 記錄查詢並取得實例呼叫，請使用下列登錄機碼值。 記錄檔將會位於記錄檔資料夾中，而且將會是預設的檔案大小。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** 檔 \\  = C： \\ Windows \\ system32 \\ WBEM \\ 記錄 \\ ViewProvider .log

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **層級**= 2

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **MaxFileSize** = 65535

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **提供者** \\ **記錄** \\ **ViewProvider** \\ **類型**= 檔案

> [!Note]  
> 針對具有記錄功能的您自己的提供者，您需要撰寫必要的登錄機碼和值以啟用記錄。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[WMI 記錄檔](wmi-log-files.md)
</dt> <dt>

[WMI 疑難排解類別](wmi-troubleshooting-classes.md)
</dt> <dt>

[追蹤 WMI 活動](tracing-wmi-activity.md)
</dt> </dl>

 

 
