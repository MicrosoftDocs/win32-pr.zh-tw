---
description: Win32 \_ ServerFeature 類別代表安裝在執行 Windows Server 之電腦上的功能。
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312135"
---
# <a name="win32_serverfeature-class"></a>Win32 \_ ServerFeature 類別

\[**Win32 \_ ServerFeature** 類別可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [ServerManager Deploymentprovider 提供者類別](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)。\]

**Win32 \_ ServerFeature** 類別代表安裝在執行 Windows Server 之電腦上的功能。

開發人員和系統管理員可以使用這個類別，將判斷安裝在一組伺服器電腦上的功能自動化。 用戶端電腦上無法使用這個類別的實例。

## <a name="syntax"></a>語法

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>成員

**Win32 \_ ServerFeature** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ServerFeature** 類別具有這些屬性。

<dl> <dt>

**識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](key-qualifier.md)， [**非 \_ Null**](optional-qualifiers.md)
</dt> </dl>

伺服器功能識別碼。 下列清單顯示 [識別碼] 屬性的可能值：



值

名稱

1

[應用程式伺服器](/windows)

2

Web 伺服器 (IIS)

3

[串流處理媒體服務](/windows)

5

傳真伺服器

6

檔案和 iSCSI 服務<br/> [名稱變更](/windows)<br/>

7

列印和文件服務<br/> [名稱變更](/windows)<br/>

8

[Active Directory 同盟服務](/windows)

9

Active Directory 輕量型目錄服務

10

Active Directory Domain Services

11

[UDDI 服務](/windows)<br/>

12

[DHCP 伺服器](/windows)

13

[DNS 伺服器](/windows)

14

Network Policy and Access Services

16

Active Directory 憑證服務

17

Active Directory Rights Management Services

18

[遠端桌面服務](/windows)<br/> [名稱變更](/windows)<br/>

19

Windows Deployment Services

20

Hyper-V

21

[Windows Server Update Services](/windows)

33

[容錯移轉叢集](/windows)

34

[網路負載平衡](/windows)

36

[.NET Framework 3.5.1 功能](/windows)<br/> [名稱變更](/windows)<br/>

37

[Windows 系統資源管理員](/windows)

38

無線區域網路服務

39

[Windows Server Backup 功能](/windows)

40

WINS 伺服器

41

Windows 處理序啟用服務

42

[遠端協助](/windows)

43

簡單 TCP/IP 服務

44

[Telnet 用戶端](/windows)

45

[Telnet 伺服器](/windows)

46

[以 Unix 為基礎的應用程式子系統](/windows)

47

RPC Over HTTP Proxy

48

SMTP 伺服器

49

訊息佇列

51

[Windows 內部資料庫](/windows)

52

[儲存體適用于 San 的管理員](/windows)

53

LPR 連接埠監視器

55

[Internet Storage Name Server](/windows)

57

[多重路徑 I/O](/windows)

58

TFTP 用戶端

59

[SNMP 服務](/windows)

60

[卸除式存放裝置管理員](/windows)

61

BitLocker 磁碟機加密

62

[適用于網路檔案系統的服務](/windows)

63

網際網路列印用戶端

64

[對等名稱解析通訊協定](/windows)

65

連線管理員系統管理組件

66

[Windows PowerShell](/windows)<br/>

67

[遠端伺服器管理工具](/windows)

68

[高品質 Windows 音訊/視訊體驗](/windows)

69

[群組原則管理](/windows)

71

[索引服務](/windows)

72

[檔案伺服器資源管理員 (FSRM)](/windows)

73

遠端差異壓縮

310

筆跡和手寫服務<br/>

320

[Windows Server 移轉工具](/windows)<br/>

321

[WinRM IIS 延伸模組](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[DirectAccess 管理主控台](/windows)<br/>

335

[背景智慧型傳送服務 (BITS)](/windows)<br/>

338

[XPS 檢視器](/windows)<br/>

339

[Windows 生物特徵辨識架構](/windows)<br/>

340

WoW64 支援<br/>

351

[Windows PowerShell整合式腳本環境 (ISE) ](/windows)<br/>

352

Windows TIFF IFilter<br/>

404

[Windows Server Update Services](/windows)

409

[IP 位址管理 (IPAM) 伺服器](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Windows Search 服務](/windows)

438

[Client for NFS](/windows)

441

[BitLocker 網路解除鎖定](/windows)

442

[Management OData IIS 延伸模組](/windows)

450

[.NET Framework 4.5 進階服務](/windows)

466

[.NET Framework 4.5 功能](/windows)

468

[遠端存取](/windows)<br/>

477

[使用者介面和基礎結構](/windows)

478

[圖形化管理工具與基礎結構](/windows)

481

[檔案和存放服務](/windows)

485

[Windows Server Essentials 體驗](/windows)

488

[Direct Play](/windows)

檔案服務-角色服務 (6) 

值

名稱

100

[分散式檔案系統](/windows)

101

DFS 命名空間

102

DFS 複寫

103

[檔案複寫服務](/windows)

104

[檔案伺服器資源管理員 (FSRM)](/windows)

105

[適用于網路檔案系統的服務](/windows)

106

[儲存單一版本](/windows)

107

[Windows Search 服務](/windows)

108

[索引服務](/windows)

255

檔案伺服器

350

網路檔案的 BranchCache

431

[NFS 伺服器](/windows)<br/>

434

[檔案伺服器 VSS 代理程式服務](/windows)<br/>

435

[iSCSI 目標伺服器](/windows)<br/>

436

[重複資料刪除](/windows)<br/>

437

[iSCSI 目標儲存體提供者 (VDS 和 VSS 硬體提供者) ](/windows)

486

[工作資料夾](/windows)

AD DS-角色服務 (10) 

值

名稱

110

[Active Directory 網域控制站](/windows)

111

[Unix 身分識別管理](/windows)

112

[網路資訊服務的伺服器](/windows)

113

[密碼同步](/windows)

294

[遠端伺服器管理工具](/windows)

串流處理媒體-角色服務 (3) 

值

名稱

120

[Windows媒體伺服器](/windows)

121

[以網路為基礎的系統管理](/windows)

122

[記錄代理程式](/windows)

ADFS-角色服務 (8) 

值

名稱

125

[Active Directory 同盟服務](/windows)

126

[同盟服務原則](/windows)

127

[AD FS 網頁代理程式](/windows)

128

[宣告感知代理程式](/windows)

129

[Windows以權杖為基礎的代理程式](/windows)

遠端桌面服務-角色服務 (18) 

值

名稱

130

遠端桌面工作階段主機<br/> [名稱變更](/windows)<br/>

131

[遠端桌面授權](/windows)<br/> [名稱變更](/windows)<br/>

132

遠端桌面閘道<br/> [名稱變更](/windows)<br/>

133

遠端桌面連線代理人<br/> [名稱變更](/windows)<br/>

134

遠端桌面 Web 存取<br/> [名稱變更](/windows)<br/>

322

遠端桌面虛擬主機<br/>

遠端桌面虛擬化主機-角色服務 (322) 

值

名稱

325

[核心服務](/windows)<br/>

327

[遠端桌面虛擬圖形](/windows)<br/>

列印和檔服務-角色服務 (7) 

值

名稱

135

列印伺服器

136

網際網路列印

137

LPD 列印服務

328

[分散式掃描伺服器](/windows)<br/>

Web 服務器 (IIS) -角色服務 (2) 

值

名稱

140

Web 伺服器

141

一般 HTTP 功能

142

靜態內容

143

預設文件

144

瀏覽目錄

145

HTTP 錯誤

146

HTTP 重新導向

147

應用程式開發

148

ASP.NET

149

.NET 擴充性

150

ASP

151

CGI

152

ISAPI 擴充程式

153

ISAPI 篩選

154

伺服器端包含

155

健康情況和診斷

156

HTTP 記錄

157

記錄工具

158

要求監視器

159

追蹤

160

自訂記錄

161

ODBC 記錄

162

安全性

163

基本驗證

164

Windows 驗證

165

摘要式驗證

166

用戶端憑證對應驗證

167

IIS 用戶端憑證對應驗證

168

URL 授權

169

要求篩選

170

IP 和網域限制

171

效能

172

靜態內容壓縮

173

動態內容壓縮

174

管理工具

175

IIS 管理主控台

176

IIS 管理腳本和工具

177

Management Service

178

IIS 6 管理相容性

179

IIS 6 Metabase 相容性

180

IIS 6 WMI 相容性

181

IIS 6 指令碼工具

182

IIS 6 管理主控台

183

FTP 發行服務<br/>

184

FTP 伺服器

185

FTP 管理主控台<br/>

314

WebDAV 發行

316

FTP 服務<br/>

317

FTP 擴充性<br/>

336

可裝載 IIS 的 Web 核心<br/>

413

[ASP.NET 4.5](/windows)

414

[.NET 擴充性 4.5](/windows)

445

[appialization](/windows)

446

[集中式 SSL 憑證支援](/windows)

447

[WebSocket 通訊協定](/windows)

訊息佇列-功能 (49) 

值

名稱

190

訊息佇列服務

191

訊息佇列伺服器

192

目錄服務整合

193

訊息佇列觸發程序

194

HTTP 支援

195

路由服務

196

[Windows 2000 用戶端支援](/windows)<br/>

197

訊息佇列 DCOM Proxy

228

多點傳送支援

Active Directory 憑證服務-角色服務 (16) 

值

名稱

200

憑證授權單位

201

憑證授權單位網頁註冊。

202

線上回應

204

網路裝置註冊服務

318

[憑證註冊 Web 服務](/windows)<br/>

319

[憑證註冊原則 Web 服務](/windows)<br/>

網路原則和 Access Services 角色服務 (14) 

值

名稱

205

[網路原則伺服器](/windows)

206

[VPN](#vpn)

207

[遠端 Access Services](/windows)

208

[路由](#routing)

210

[健康情況登錄授權單位](/windows)

250

[主機認證授權通訊協定](/windows)

UDDI 服務-角色服務 (11) 

值

名稱

215

[UDDI 服務 Web 應用程式](/windows)<br/>

216

[UDDI 服務資料庫](/windows)<br/>

Windows進程啟用服務-角色服務 (41) 

值

名稱

217

設定 API

218

.NET 環境

219

處理序模型

.NET Framework 3.5.1-功能 (36) 

值

名稱

220

.NET Framework 3.5.1<br/> [名稱變更](/windows)<br/>

221

WCF 啟用

222

HTTP 啟動

223

非 HTTP 啟用

227

XPS 檢視器<br/>

SNMP 服務-功能 (59) 

值

名稱

224

[SNMP 服務](/windows)

225

[SNMP WMI 提供者](/windows)

應用程式服務-角色服務

值

名稱

230

[.NET Framework 3.5。1](/windows)<br/> [名稱變更](/windows)<br/>

231

[網頁伺服器 (IIS) 支援](/windows)

232

[COM + 網路存取](/windows)

233

[TCP 連接埠共用](/windows)

234

[Windows 處理程序啟動服務支援](/windows)

235

[HTTP 啟動](/windows)

236

[訊息佇列啟動](/windows)

237

[TCP 啟用](/windows)

238

[具名管道啟動](/windows)

239

[分散式交易](/windows)

240

[傳入遠端交易](/windows)

241

[連出遠端交易](/windows)

242

[WS-自動交易](/windows)

353

[適用于 .NET 4.0 的應用程式伺服器擴充功能](/windows)<br/>

Windows部署服務-角色 (19) 

值

名稱

251

部署伺服器

252

傳輸伺服器

Active Directory Rights Management Services-角色服務 (17) 

值

名稱

253

Active Directory Rights Management Server

254

識別身分同盟支援

遠端伺服器管理工具 (67) 

值

名稱

256

[角色管理工具](/windows)

257

[AD DS 工具](/windows)<br/> [名稱變更](/windows)<br/>

258

[AD LDS Snap-Ins 和 Command-Line 工具](/windows)<br/> [名稱變更](/windows)<br/>

259

Active Directory 憑證服務工具

260

[Network Policy and Access Services](/windows)

261

列印和檔服務工具<br/> [名稱變更](/windows)<br/>

262

[Active Directory Rights Management Services](/windows)

263

[遠端桌面服務工具](/windows)<br/> [名稱變更](/windows)<br/>

264

Windows 部署服務工具

265

[功能管理工具](/windows)

266

BitLocker 磁碟機加密工具

267

BITS 伺服器擴充功能工具

268

[容錯移轉叢集工具](/windows)

269

網路負載平衡工具

270

SMTP 伺服器工具

273

[DNS 伺服器工具](/windows)

277

檔案服務工具

278

分散式檔案系統工具

279

檔案伺服器 Resource Manager 工具

280

[Services For Network File System 工具](/windows)

281

Web 服務器 (IIS) 工具

284

[遠端桌面工作階段主機工具](/windows)<br/> [名稱變更](/windows)<br/>

285

遠端桌面閘道工具<br/> [名稱變更](/windows)<br/>

286

遠端桌面授權工具<br/> [名稱變更](/windows)<br/>

288

傳真伺服器工具

290

WINS 伺服器工具

291

[UDDI 服務工具](/windows)<br/>

292

憑證授權單位單位工具

293

線上回應工具

297

[Server for NIS 工具](/windows)

299

[AD DS Snap-Ins 和 Command-Line 工具](/windows)<br/> [名稱變更](/windows)<br/>

300

[ Active Directory 管理中心](/windows)

301

Hyper-v 工具

323

[BitLocker 修復密碼檢視器](/windows)<br/>

326

[BitLocker 磁碟機加密管理公用程式](/windows)<br/>

329

[AD DS 和 AD LDS 工具](/windows)<br/>

330

Active Directory 管理中心<br/>

331

[適用於 Windows PowerShell 的 Active Directory 模組](/windows)<br/>

337

[遠端桌面連線代理人工具](/windows)<br/>

410

[IP 位址管理 (IPAM) 用戶端](/windows)

450

[Windows PowerShell 的 Hyper-V 模組](/windows)

462

[Active Directory Rights Management Services工具](/windows)

465

[共用和儲存體管理工具](/windows)

471

[遠端存取管理工具](/windows)

472

[適用於 Windows PowerShell 的遠端存取模組](/windows)

473

[遠端存取 GUI 和 Command-Line 工具](/windows)

474

[Windows Server Update Services 工具](/windows)

476

[遠端桌面授權診斷程式工具](/windows)

479

[SNMP 工具](/windows)

480

[大量啟用工具](/windows)

Windows伺服器備份-功能 (39) 

值

名稱

296

[Windows Server Backup](/windows)

297

[命令列工具](/windows)

筆跡和手寫服務-功能 (310) 

值

名稱

311

[筆跡支援](/windows)<br/>

312

[手寫辨識](/windows)<br/>

背景智慧型傳送服務 (位) -功能 (335) 

值

名稱

54

IIS 伺服器擴充功能

332

[Compact Server](/windows)<br/>

Wow64 支援-功能 (340) 

值

名稱

341

[WoW64](#wow64)<br/>

342

[.NET Framework 2.0 和 Windows PowerShell 的 WoW64](/windows)<br/>

343

[.NET Framework 2.0 的 WoW64](/windows)<br/>

344

[適用于 PowerShell 的 WoW64](/windows)<br/>

345

[.NET Framework 3.0 和3.5 的 WoW64](/windows)<br/>

346

[列印服務的 WoW64](/windows)<br/>

347

[用於容錯移轉叢集的 WoW64](/windows)<br/>

348

[輸入法編輯器的 WoW64](/windows)<br/>

349

[適用于 UNIX 應用程式之子系統的 WoW64](/windows)<br/>

使用者介面和基礎結構-角色服務 (447) 

值

名稱

35

[桌面體驗](/windows)

99

[伺服器圖形化 Shell](/windows)

Windows Server Update Services-功能 (404) 

值

名稱

405

[API 和 PowerShell Cmdlet](/windows)

406

[SQL Server連接](/windows)

407

[WSUS 服務](/windows)

408

[消費者介面管理主控台](/windows)

449

[WID 連線能力](/windows)

Windows PowerShell-功能 (417) 

值

名稱

411

[Windows PowerShell 2.0 引擎](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Windows PowerShell Web 存取](/windows)

1000

[Windows PowerShell Desired State Configuration 服務](/windows)

.NET Framework 4.5-功能 (418) 

值

名稱

419

[.NET Framework 4.5 擴充](/windows)

420

[WCF 服務](/windows)

421

[HTTP 啟動](/windows)

422

[訊息佇列 (MSMQ) 啟用](/windows)

423

[具名管道啟用](/windows)

424

[TCP 啟用](/windows)

425

[TCP 連接埠共用](/windows)

429

[ASP.NET 4.5](/windows)

遠端存取-角色 (468) 

值

名稱

469

[DirectAccess 和 VPN (RAS) ](/windows)

470

[路由](#routing)

檔案和儲存體服務-角色 (481) 

值

名稱

482

[儲存體服務](/windows)

484

[容錯移轉叢集管理工具](/windows)



 

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

伺服器功能的顯示名稱，例如「檔案伺服器」、「列印伺服器」或「桌面體驗」。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

父伺服器功能的識別碼。 如果類別的目前實例所代表的功能沒有父項功能，則這個屬性為0。

</dd> </dl>

## <a name="remarks"></a>備註

閱讀[Windows server 2008 伺服器管理員技術總覽](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10))，以瞭解伺服器功能。

不使用管理軟體（例如安裝的管理元件 System Center Operations Manager）的企業，可以藉由查詢 **Win32 \_ ServerFeature** 類別來取得該資訊。

您可以使用 WMI 或 WinRM 的遠端功能，從遠端伺服器取得伺服器功能資訊。 如需遠端 WMI DCOM 連接的詳細資訊，請參閱 [連接到遠端電腦上的 wmi](connecting-to-wmi-on-a-remote-computer.md)。 如需有關 WinRM 的詳細資訊，請參閱 Windows 遠端管理。

Windows Server 2012： **Win32 \_ ServerFeature** 已被取代。 若要以程式設計方式存取 windows server 功能資訊，您可以使用 [伺服器管理員 Cmdlet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))。

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>應用程式伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>串流媒體服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory 同盟服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP 伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS 伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>遠端桌面服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

不再支援

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>容錯移轉叢集
</dt> <dd>

不再支援

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>網路負載平衡
</dt> <dd>

不再支援

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 功能
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows系統 Resource Manager
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows伺服器備份功能
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>遠端協助
</dt> <dd>

不再支援

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet 用戶端
</dt> <dd>

不再支援

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet 伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>以 Unix 為基礎的應用程式子系統
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows 內部資料庫
</dt> <dd>

不再支援

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>儲存體適用于 San 的管理員
</dt> <dd>

不再支援

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>網際網路儲存體名稱伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>多重路徑 i/o
</dt> <dd>

不再支援

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP 服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>適用于網路檔案系統的服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>對等名稱解析通訊協定
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>遠端伺服器管理工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>品質 Windows 音效影片體驗
</dt> <dd>

不再支援

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>群組原則管理
</dt> <dd>

不再支援

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>索引服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>檔案伺服器 Resource Manager (FSRM) 
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows伺服器遷移工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache
</dt> <dd>

不再支援

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess 管理主控台
</dt> <dd>

不再支援

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>背景智慧型傳送服務 (位) 
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 支援
</dt> <dd>

不再支援

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

已新增

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP 位址管理 (IPAM) Server
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

已新增

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4。5
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows搜尋服務
</dt> <dd>

已新增

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>NFS 用戶端
</dt> <dd>

已新增

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker 網路解除鎖定
</dt> <dd>

已新增

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>管理 OData IIS 擴充功能
</dt> <dd>

已新增

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services
</dt> <dd>

已新增

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 功能
</dt> <dd>

已新增

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>使用者介面和基礎結構
</dt> <dd>

已新增

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>圖形化管理工具與基礎結構
</dt> <dd>

已新增

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>檔案和儲存體服務
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>WindowsServer Essentials 體驗
</dt> <dd>

已新增

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>直接播放
</dt> <dd>

已新增

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>分散式檔案系統
</dt> <dd>

不再支援

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>檔案伺服器 Resource Manager
</dt> <dd>

不再支援

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>適用于網路檔案系統的服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>單一實例儲存體
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows搜尋服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>索引服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI 目標儲存體提供者 (VDS 和 VSS 硬體提供者) 
</dt> <dd>

已新增

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾
</dt> <dd>

已新增

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory 網網域控制站
</dt> <dd>

不再支援

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Unix 身分識別管理
</dt> <dd>

不再支援

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>網路資訊服務的伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>密碼同步化
</dt> <dd>

不再支援

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>管理工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows媒體伺服器
</dt> <dd>

不再支援。

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>以網路為基礎的系統管理
</dt> <dd>

不再支援

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>記錄代理程式
</dt> <dd>

不再支援

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>同盟服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>同盟服務原則
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web 代理程式
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows以權杖為基礎的代理程式
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>遠端桌面授權
</dt> <dd>

不再支援

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>網路原則伺服器
</dt> <dd>

不再支援

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>Vpn
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>遠端 Access Services
</dt> <dd>

不再支援

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>路由
</dt> <dd>

不再支援

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>健康情況登錄授權單位
</dt> <dd>

不再支援

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>主機認證授權通訊協定
</dt> <dd>

不再支援

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5。1
</dt> <dd>

不再支援

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS 檢視器
</dt> <dd>

不再支援

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP 服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI 提供者
</dt> <dd>

不再支援

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5。1
</dt> <dd>

不再支援

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span> (IIS) 支援的 Web 服務器
</dt> <dd>

不再支援

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM + 網路存取
</dt> <dd>

不再支援

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP 埠共用
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows處理常式啟用服務支援
</dt> <dd>

不再支援

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP 啟用
</dt> <dd>

不再支援

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>訊息佇列啟用
</dt> <dd>

不再支援

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP 啟用
</dt> <dd>

不再支援

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>具名管道啟用
</dt> <dd>

不再支援

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>分散式交易
</dt> <dd>

不再支援

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>傳入遠端交易
</dt> <dd>

不再支援

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>連出遠端交易
</dt> <dd>

不再支援

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-自動交易
</dt> <dd>

不再支援

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>適用于 .NET 4.0 的應用程式伺服器擴充功能
</dt> <dd>

不再支援

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>角色管理工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins 和 Command-Line 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>網路原則和 Access Services
</dt> <dd>

不再支援

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>遠端桌面服務工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>功能管理工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>容錯移轉叢集工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS 伺服器工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web 服務器 (IIS) 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins 和 Command-Line 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>遠端桌面連線代理人工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP 位址管理 (IPAM) 用戶端
</dt> <dd>

已新增

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Windows PowerShell 的 hyper-v 模組
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>共用和儲存體管理工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>遠端存取管理工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Windows PowerShell 的遠端存取模組
</dt> <dd>

已新增

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>遠端存取 GUI 和 Command-Line 工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>遠端桌面授權診斷程式工具
</dt> <dd>

已新增

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP 工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>大量啟用工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows伺服器備份
</dt> <dd>

不再支援

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>命令列工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>筆跡支援
</dt> <dd>

不再支援

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>手寫辨識
</dt> <dd>

不再支援

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>適用于 .NET Framework 2.0 和 PowerShell 的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>.NET Framework 2.0 的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>適用于 PowerShell 的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>.NET Framework 3.0 和3.5 的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>列印服務的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>用於容錯移轉叢集的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>輸入法編輯器的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>適用于 UNIX 應用程式之子系統的 WoW64
</dt> <dd>

不再支援

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>桌面體驗
</dt> <dd>

已新增

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>伺服器圖形化 Shell
</dt> <dd>

已新增

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API 和 PowerShell Cmdlet
</dt> <dd>

已新增

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server連接
</dt> <dd>

已新增

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS 服務
</dt> <dd>

已新增

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>消費者介面管理主控台
</dt> <dd>

已新增

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID 連線能力
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 引擎
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3。0
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShellWeb 存取
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration 服務
</dt> <dd>

已新增

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 擴充
</dt> <dd>

已新增

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF 服務
</dt> <dd>

已新增

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP 啟用
</dt> <dd>

已新增

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>訊息佇列 (MSMQ) 啟用
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>具名管道啟用
</dt> <dd>

已新增

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP 啟用
</dt> <dd>

已新增

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP 埠共用
</dt> <dd>

已新增

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4。5
</dt> <dd>

已新增

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET 擴充性4。5
</dt> <dd>

已新增

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess 和 VPN (RAS) 
</dt> <dd>

已新增

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>路由
</dt> <dd>

已新增

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>儲存體服務
</dt> <dd>

已新增

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>容錯移轉叢集管理工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>應用程式初始化
</dt> <dd>

已新增

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>集中式 SSL 憑證支援
</dt> <dd>

已新增

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>宣告感知代理程式
</dt> <dd>

不再支援

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>遠端桌面工作階段主機工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket 通訊協定
</dt> <dd>

不再支援

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM + 網路存取
</dt> <dd>

不再支援

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>檔案和 iSCSI 服務名稱變更
</dt> <dd>

已變更為檔案服務

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>使用者介面和基礎結構
</dt> <dd>

已新增

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS
</dt> <dd>

已新增

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>檔案伺服器 VSS 代理程式服務
</dt> <dd>

已新增

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI 目標伺服器
</dt> <dd>

已新增

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>重復資料刪除
</dt> <dd>

已新增

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾
</dt> <dd>

移除

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>核心服務
</dt> <dd>

僅針對此版本新增。

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>遠端桌面虛擬圖形
</dt> <dd>

僅針對此版本新增

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>遠端存取
</dt> <dd>

已新增

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI 服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows系統 Resource Manager
</dt> <dd>

不再支援

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>可移動儲存體管理員
</dt> <dd>

不再支援

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

不再支援

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>筆跡和手寫服務
</dt> <dd>

已新增

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS 擴充功能
</dt> <dd>

已新增

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess 管理主控台
</dt> <dd>

已新增

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>背景智慧型傳送服務 (位) 
</dt> <dd>

已新增

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS 檢視器
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows生物特徵辨識架構
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 支援
</dt> <dd>

已新增

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell整合式腳本環境 (ISE) 
</dt> <dd>

已新增

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>檔案複寫服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>網路檔案的 BranchCache
</dt> <dd>

已新增

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>工作資料夾
</dt> <dd>

已新增

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>分散式掃描伺服器
</dt> <dd>

已新增

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP 發行服務
</dt> <dd>

不再支援

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP 管理主控台
</dt> <dd>

不再支援

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP 服務
</dt> <dd>

已新增

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP 擴充性
</dt> <dd>

已新增

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS 裝載的 Web 核心
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 用戶端支援
</dt> <dd>

不再支援

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>憑證註冊 Web 服務
</dt> <dd>

已新增

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>憑證註冊原則 Web 服務
</dt> <dd>

已新增

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI 服務 Web 應用程式
</dt> <dd>

不再支援

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI 服務資料庫
</dt> <dd>

不再支援

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>適用于 .NET 4.0 的應用程式伺服器擴充功能
</dt> <dd>

已新增

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI 服務工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker 磁碟機加密管理公用程式
</dt> <dd>

已新增

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具
</dt> <dd>

不再支援

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS 和 AD LDS 工具
</dt> <dd>

已新增

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory 管理中心
</dt> <dd>

已新增

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>適用于 Windows PowerShell 的 Active Directory 模組
</dt> <dd>

已新增

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>遠端桌面連線代理人工具
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>.NET Framework 2.0 和 Windows PowerShell 的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>.NET Framework 2.0 的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>適用于 PowerShell 的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>.NET Framework 3.0 和3.5 的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>列印服務的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>用於容錯移轉叢集的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>輸入法編輯器的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>適用于 UNIX 應用程式之子系統的 WoW64
</dt> <dd>

已新增

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker 修復密碼檢視器
</dt> <dd>

已新增

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>列印和檔服務名稱變更
</dt> <dd>

此版本的命名列印服務

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>遠端桌面服務名稱變更
</dt> <dd>

此版本中命名的終端機服務

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 功能名稱變更
</dt> <dd>

此版本中的命名 .NET Framework 3.0 功能

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>遠端桌面工作階段主機名稱變更
</dt> <dd>

此版本中命名的終端機伺服器

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>遠端桌面授權名稱變更
</dt> <dd>

此版本中的命名為 TS 授權

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>遠端桌面閘道名稱變更
</dt> <dd>

此版本中的命名為 TS 閘道

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>遠端桌面連線代理人名稱變更
</dt> <dd>

此版本中的命名為 TS Session Broker

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>遠端桌面 Web 存取名稱變更
</dt> <dd>

此版本中名為 TS Web 存取

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 名稱變更
</dt> <dd>

此版本中名為 Net FX 3.0 功能的 (220) 

在此版本中，名為 Application Server Core 的 (230) 

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS 工具名稱變更
</dt> <dd>

此版本中的命名 Active Directory Domain Services 工具

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins 和 Command-Line 工具名稱變更
</dt> <dd>

此版本中的命名 Active Directory 輕量型目錄服務工具

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>列印和檔服務工具名稱變更
</dt> <dd>

此版本中的命名列印服務工具

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>遠端桌面服務工具名稱變更
</dt> <dd>

此版本中命名的終端機服務工具

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>遠端桌面工作階段主機工具名稱變更
</dt> <dd>

此版本中命名的終端機伺服器工具

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>遠端桌面閘道工具名稱變更
</dt> <dd>

此版本中命名的 TS 閘道工具

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>遠端桌面授權工具名稱變更
</dt> <dd>

此版本中命名的 TS 授權工具

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins 和 Command-Line 工具名稱變更
</dt> <dd>

Active Directory 網域控制站工具

</dd> </dl>

## <a name="examples"></a>範例

下列腳本會顯示名為 "FABRIKAM" 的電腦上所有伺服器功能的名稱。 請注意，目的電腦必須執行 Windows server 2008 或更新版本的伺服器作業系統。


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

