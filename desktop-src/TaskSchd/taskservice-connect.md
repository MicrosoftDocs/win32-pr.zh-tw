---
title: TaskService 方法
description: 針對腳本，連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Connect 方法工作排程器
- Connect 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，Connect 方法
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934139"
---
# <a name="taskserviceconnect-method"></a>TaskService 方法

針對腳本，連接至遠端電腦，並將此介面上的所有後續呼叫與遠端會話產生關聯。 如果 serverName 參數是空的，則這個方法會在本機電腦上執行。 如果未指定 userId，則會使用目前的權杖。

## <a name="syntax"></a>語法


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*serverName* \[在中，選擇性\]
</dt> <dd>

您要連接的電腦名稱稱。 如果 serverName 參數是空的，則這個方法會在本機電腦上執行。

</dd> <dt>

*使用者* \[在中，選擇性\]
</dt> <dd>

連接到電腦時使用的使用者名稱。 如果未指定使用者，則會使用目前的權杖。

</dd> <dt>

*網域* \[在中，選擇性\]
</dt> <dd>

*使用者* 參數中所指定之使用者的網域。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

用來連接到電腦的密碼。 如果未指定使用者名稱和密碼，則會使用目前的權杖。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫任何其他 [**TaskService**](taskservice.md)方法之前，應該先呼叫 **TaskService** 方法。

如果 Connect 方法失敗，您可以收集錯誤識別碼以找出錯誤的意義。 下表列出錯誤識別碼及其描述。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>錯誤識別碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>拒絕存取以連接到工作排程器服務。</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>工作排程器服務未執行。</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>應用程式沒有足夠的記憶體可完成作業，或者 <em>使用者</em>、 <em>密碼</em>或 <em>網域</em> 至少有一個 null 和一個非 null 值。</td>
</tr>
<tr class="even">
<td>53</td>
<td>在下列情況下，會傳回此錯誤：
<ul>
<li><em>ServerName</em>參數中指定的電腦名稱稱不存在。</li>
<li>當您嘗試連線到 Windows Server 2003 或 Windows XP 電腦，而且遠端電腦未啟用 [檔案和印表機共用] 防火牆例外，或遠端登入服務未執行時。</li>
<li>當您嘗試連線到 Windows Vista 電腦時，如果遠端電腦未啟用 [遠端排程工作] 管理防火牆例外，且已啟用 [檔案及印表機共用] 防火牆例外，或遠端登入服務未執行。</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>從 Windows Vista 電腦連線到遠端 Windows XP 或 Windows Server 2003 電腦時，無法指定 <em>使用者</em>、 <em>密碼</em>或 <em>網域</em> 參數。</td>
</tr>
</tbody>
</table>



 

如果您是從 Windows Vista 連接到遠端 Windows Vista 電腦，則需要允許遠端電腦上的遠端排程工作管理防火牆例外。 若要允許此例外，請依序按一下 [開始]、[控制台]、[安全性]、[允許程式通過 Windows 防火牆]，然後選取 [遠端排程工作管理] 核取方塊。 接著按一下 [Windows 防火牆設定] 對話方塊中的 [確定] 按鈕。

如果您是從 Windows Vista 電腦連線到遠端 Windows XP 或 Windows Server 2003 電腦，則需要允許遠端電腦上的 [檔案及印表機共用] 防火牆例外。 若要允許此例外，請依序按一下 [開始]、[控制台]，按兩下 [Windows 防火牆]，選取 [例外] 索引標籤，然後選取 [檔案及印表機共用] 防火牆例外。 然後按一下 [Windows 防火牆] 對話方塊中的 [確定] 按鈕。 遠端登入服務也必須在遠端電腦上執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





