---
title: 收集 User-Mode 傾印
description: 從 Windows Server 2008 和 Windows Vista （含 Service Pack 1 (SP1) ）開始，可以設定 Windows 錯誤報告 (WER) ，以便在使用者模式應用程式損毀之後，收集完整的使用者模式傾印並儲存在本機。
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4597c4bf1fd583b647e7ad74b7f1cb2cd41be9c0118226d502932c61f481cedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442362"
---
# <a name="collecting-user-mode-dumps"></a>收集 User-Mode 傾印

從 Windows Server 2008 和 Windows Vista （含 Service Pack 1 (SP1) ）開始，可以設定 Windows 錯誤報告 (WER) ，以便在使用者模式應用程式損毀之後，收集完整的使用者模式傾印並儲存在本機。 這項功能不支援自行自訂損毀報告（包括 .NET 應用程式）的應用程式。

預設不會啟用此功能。 啟用此功能需要系統管理員許可權。 若要啟用並設定此功能，請使用 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ Windows 錯誤報告 \\ LocalDumps** 機碼底下的下列登錄值。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
<th>類型</th>
<th>預設值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DumpFolder</strong></td>
<td>要儲存傾印檔案的路徑。 如果您未使用預設路徑，請確定該資料夾包含允許損毀進程將資料寫入資料夾的 Acl。 針對服務損毀，會根據所使用的服務帳戶，將傾印寫入服務特定的設定檔資料夾。 例如，系統服務的設定檔資料夾是%WINDIR%\System32\Config\SystemProfile。 針對網路和本機服務，此資料夾為%WINDIR%\ServiceProfiles。<br/></td>
<td> REG_EXPAND_SZ </td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>資料夾中傾印檔案的最大數目。 當超過最大值時，資料夾中最舊的傾印檔案將會取代為新的傾印檔案。</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>指定下列其中一種傾印類型：
<ul>
<li>0：自訂傾印</li>
<li>1：迷你傾印</li>
<li>2：完整傾印</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>要使用的自訂傾印選項。 只有當 <strong>DumpType</strong> 設為0時，才會使用這個值。<br/> 這些選項是 <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> 列舉值的位元組合。<br/></td>
<td>REG_DWORD</td>
 <td><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> 當您 [為 **應用程式**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)損毀設定自動偵測時，不會收集損毀傾印。 

這些登錄值代表全域設定。 您也可以提供覆寫全域設定的每個應用程式設定。 若要建立每個應用程式的設定，請在 **HKEY \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Windows 錯誤報告 \\ LocalDumps** (例如 **HKEY \_ local \_ machine \\ software \\ microsoft \\ Windows \\ Windows 錯誤報告 \\ LocalDumps \\MyApplication.exe**) 中，為您的應用程式建立新的金鑰。 在 **MyApplication.exe** 機碼下新增傾印設定。 如果您的應用程式當機，則 WER 會先讀取全域設定，然後使用您的應用程式特定設定來覆寫任何設定。

當應用程式損毀並在終止之前，系統會檢查登錄設定，以判斷是否要收集本機傾印。 傾印收集完成後，應用程式就可以正常終止。 如果應用程式支援復原，則在呼叫復原回呼之前，會先收集本機傾印。

這些傾印會獨立于 WER 基礎結構的其餘部分來設定和控制。 即使已停用 WER 或使用者取消 WER 報表，您也可以使用本機傾印集合。 本機傾印可能不同于傳送給 Microsoft 的傾印。

 

