---
title: 桌面安全性與存取權限
description: 安全性可讓您控制對桌面物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375960"
---
# <a name="desktop-security-and-access-rights"></a>桌面安全性與存取權限

安全性可讓您控制對桌面物件的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

當您呼叫 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)或 [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)函式時，可以指定桌面物件的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。 如果您指定 Null，桌面會取得預設安全描述項。 桌面預設安全描述項中的 Acl 來自于其父視窗工作站。

若要取得或設定視窗站物件的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

當您呼叫 [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) 或 [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。

桌面物件的有效存取權限包括 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及某些特定物件的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                       | 意義                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 刪除 (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                       |
| 讀取 \_ 控制 (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求存取 \_ 系統 \_ 安全性存取權限。 如需詳細資訊，請參閱 [SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權。 |
| 同步處理 (0x00100000L)    | 不支援桌面物件。                                                                                                                                                                                                                                                   |
| 撰寫 \_ DAC (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                               |
| 撰寫 \_ 擁有者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                              |



 

下表列出特定物件的存取權限。



| 存取權限                       | Description                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ CREATEMENU (0x0004L)       | 在桌面上建立功能表所需。                                                   |
| 桌上型電腦 \_ CREATEWINDOW (0x0002L)     | 需要在桌面上建立視窗。                                                 |
| 桌面 \_ 列舉 (0x0040L)        | 要列舉桌面的必要參數。                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)      | 建立任何視窗勾點所需。                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L)  | 在桌面上執行日誌播放所需。                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)    | 在桌上型電腦上執行日誌記錄的必要。                                         |
| DESKTOP \_ READOBJECTS (0x0001L)      | 讀取桌面上的物件所需。                                                    |
| DESKTOP \_ SWITCHDESKTOP (0x0100L)    | 必須使用 [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) 函式來啟動桌面。 |
| DESKTOP \_ WRITEOBJECTS (0x0080L)     | 需要在桌上型電腦上撰寫物件。                                                   |



 

以下是使用者登入會話的互動式視窗工作站中包含的桌面物件 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。



<table>
<thead>
<tr class="header">
<th>存取權限</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

\_ \_ 如果您想要讀取或寫入物件的 SACL，您可以向桌面物件要求存取系統安全性存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

 

 