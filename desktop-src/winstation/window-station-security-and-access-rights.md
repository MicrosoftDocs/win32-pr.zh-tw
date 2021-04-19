---
title: Windows 工作站安全性與存取權限
description: 安全性可讓您控制對 window 站物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968907"
---
# <a name="window-station-security-and-access-rights"></a>Windows 工作站安全性與存取權限

安全性可讓您控制對 window 站物件的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

當您呼叫 [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)函式時，可以指定視窗站物件的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。 如果您指定 Null，則視窗站會取得預設安全描述項。 視窗工作站之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取得或設定視窗站物件的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

當您呼叫 [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。

Windows 工作站物件的有效存取權限包括 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及某些特定物件的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                       | 意義                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 刪除 (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                       |
| 讀取 \_ 控制 (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求存取 \_ 系統 \_ 安全性存取權限。 如需詳細資訊，請參閱 [SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權。 |
| 同步處理 (0x00100000L)    | 不支援 window 站物件。                                                                                                                                                                                                                                            |
| 撰寫 \_ DAC (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                               |
| 撰寫 \_ 擁有者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                              |



 

下表列出特定物件的存取權限。



| 存取權限                        | Description                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ 所有 \_ 存取 (0x37F)          | 視窗工作站的所有可能存取權限。                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)    | 使用剪貼簿所需。                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L)  | 操作全域原子的必要參數。                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)      | 需要在視窗工作站上建立新的桌面物件。                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)       | 列舉現有桌面物件所需。                                                                                                                                                                                                                               |
| WINSTA \_ 列舉 (0x0100L)          | 要列舉之視窗工作站的必要參數。                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)        | 成功呼叫 [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) 或 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函數所需。 使用者可以共用視窗工作站，而這種存取類型可以防止視窗工作站的其他使用者登出視窗工作站擁有者。 |
| WINSTA \_ READATTRIBUTES (0x0002L)     | 讀取視窗站物件的屬性時需要。 此屬性包含色彩設定和其他全域視窗工作站屬性。                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)         | 存取螢幕內容所需。                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)    | 修改視窗工作站物件的屬性時所需。 這些屬性包括色彩設定和其他全域視窗工作站屬性。                                                                                                                               |



 

以下是互動式視窗工作站物件的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) ，也就是指派給互動式使用者登入會話的視窗站。



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

以下是非互動式視窗工作站物件的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。 系統會將非互動式視窗工作站指派給互動式使用者以外的所有登入會話。



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
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

\_ \_ 如果您想要讀取或寫入物件的 SACL，您可以向 windows 工作站物件要求存取系統安全性存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

 

 