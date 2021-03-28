---
description: 捕獲全域 Shell 設定。
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: 'IShellDispatch4. GetSetting 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 755ee1d2bbd5026b1cc3ca165649e0fcb4ab20ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972365"
---
# <a name="ishelldispatch4getsetting-method"></a>IShellDispatch4. GetSetting 方法

捕獲全域 Shell 設定。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>參數

<dl> <dt>

*lSetting* \[在\]
</dt> <dd>

類型： **long**

值，指定要取出的目前 Shell 設定。 每次呼叫中只能取出一個設定。 此方法可辨識下列值。

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_AUTOCHECKSELECT** (0x00800000) 


</dt> <dd>

**Windows Vista**（含）以後版本。 [ **使用核取方塊來選取專案** ] 選項的狀態。 當系統已設定畫筆輸入裝置時，會自動啟用此選項。

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_DESKTOPHTML** (0x00000200) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_DONTPRETTYPATH** (0x00000800) 


</dt> <dd>

[ **允許所有大寫名稱** ] 選項的狀態。 從 Windows Vista，此資料夾選項已無法再使用。

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_DOUBLECLICKINWEBVIEW** (0x00000080) 


</dt> <dd>

**按兩下以開啟專案的狀態 (按一下以選取)** 選項。

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_篩選** (0x00010000) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_HIDDENFILEEXTS** (0x00000004) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_HIDEICONS** (0x00004000) 


</dt> <dd>

圖示的狀態會顯示在 Windows 檔案總管清單視圖中。 如果此選項為使用中，則清單視圖中不會顯示任何圖示。

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ICONSONLY** (0x01000000) 


</dt> <dd>

**Windows Vista**（含）以後版本。 顯示名稱的狀態會顯示在 Windows 檔案總管清單視圖中。 如果此選項為 [使用中]，圖示就會顯示在清單視圖中，但不會顯示名稱。

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_MAPNETDRVBUTTON** (0x00001000) 


</dt> <dd>

[ **顯示對應網路磁碟機機] 按鈕在工具列選項中** 的狀態。 在 Windows Vista 中，此選項已無法再使用。

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_NOCONFIRMRECYCLE** (0x00008000) 


</dt> <dd>

資源回收筒的 [ **顯示刪除確認] 對話方塊** 選項的狀態。

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_NONETCRAWLING** (0x00100000) 


</dt> <dd>

**自動搜尋網路資料夾和印表機** 選項的狀態。 在 Windows Vista 中，此選項已無法再使用。

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_SEPPROCESS** (0x00080000) 


</dt> <dd>

**在不同的進程選項中開機檔案夾視窗** 的狀態。

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_SERVERADMINUI** (0x00000004) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_SHOWALLOBJECTS** (0x00000001) 


</dt> <dd>

[隱藏的檔案 **和資料夾** ] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_SHOWATTRIBCOL** (0x00000100) 


</dt> <dd>

**詳細資料檢視選項中顯示檔案屬性** 的狀態。 在 Windows Vista 中，此選項已無法再使用。

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_SHOWCOMPCOLOR** (0x00000008) 


</dt> <dd>

[ **顯示已加密或壓縮的 NTFS** 檔案的色彩] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_SHOWEXTENSIONS** (0x00000002) 


</dt> <dd>

[ **隱藏已知檔案類型的副檔名** ] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_SHOWINFOTIP** (0x00002000) 


</dt> <dd>

[ **顯示資料夾和桌面專案** 的快顯描述] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_SHOWSTARTPAGE** (0x00400000) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_SHOWSUPERHIDDEN** (0x00040000) 


</dt> <dd>

[ **隱藏受保護的作業系統** 檔案] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_SHOWSYSFILES** (0x00000020) 


</dt> <dd>

[隱藏的檔案 **和資料夾** ] 選項的狀態。 在 Windows Vista 和更新版本中，這相當於 SSF \_ SHOWALLOBJECTS。 在 Windows Vista 之前的 Windows 版本中，此值指的是 [ **不要顯示隱藏的檔案和資料夾** ] 選項的狀態。

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_SHOWTYPEOVERLAY** (0x02000000) 


</dt> <dd>

**Windows Vista**（含）以後版本。 **縮圖選項上顯示檔案圖示** 的狀態。 如果此選項為 [使用中]，當檔案提供縮圖表示時，會套用檔案類型重迭。

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_SORTCOLUMNS** (0x00000010) 


</dt> <dd>

未使用。

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_STARTPANELON** (0x00200000) 


</dt> <dd>

Windows XP 顯示選項的狀態，會在 Windows XP 樣式和傳統樣式之間進行選取。 在 Windows Vista 中，此選項已無法再使用。

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_WEB** (0x00020000) 


</dt> <dd>

**顯示為 web view 選項** 的狀態。 在 Windows Vista 中，此選項已無法再使用。

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_WIN95CLASSIC** (0x00000400) 


</dt> <dd>

**傳統樣式** 選項的狀態。 在 Windows Vista 中，此選項已無法再使用。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

Type： **VARIANT \_ BOOL \** _

如果設定存在，則設定為 _ *true**。否則 **為 false**。

### <a name="vb"></a>VB

Type： **VARIANT \_ BOOL \** _

如果設定存在，則設定為 _ *true**。否則 **為 false**。

## <a name="examples"></a>範例

下列範例示範如何使用 JScript、VBScript 和 Visual Basic 的 **GetSetting** 。

Jscript：


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



 

 




